---
description: Класс CIM \_ Видеоконтроллер представляет возможности и управление видеоконтроллером.
ms.assetid: 7cf6bf2a-62a5-46fa-8c8f-976604360461
ms.tgt_platform: multiple
title: Класс CIM_VideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoController
- CIM_VideoController.AcceleratorCapabilities
- CIM_VideoController.Availability
- CIM_VideoController.CapabilityDescriptions
- CIM_VideoController.Caption
- CIM_VideoController.ConfigManagerErrorCode
- CIM_VideoController.ConfigManagerUserConfig
- CIM_VideoController.CreationClassName
- CIM_VideoController.CurrentBitsPerPixel
- CIM_VideoController.CurrentHorizontalResolution
- CIM_VideoController.CurrentNumberOfColors
- CIM_VideoController.CurrentNumberOfColumns
- CIM_VideoController.CurrentNumberOfRows
- CIM_VideoController.CurrentRefreshRate
- CIM_VideoController.CurrentScanMode
- CIM_VideoController.CurrentVerticalResolution
- CIM_VideoController.Description
- CIM_VideoController.DeviceID
- CIM_VideoController.ErrorCleared
- CIM_VideoController.ErrorDescription
- CIM_VideoController.InstallDate
- CIM_VideoController.LastErrorCode
- CIM_VideoController.MaxMemorySupported
- CIM_VideoController.MaxNumberControlled
- CIM_VideoController.MaxRefreshRate
- CIM_VideoController.MinRefreshRate
- CIM_VideoController.Name
- CIM_VideoController.NumberOfVideoPages
- CIM_VideoController.PNPDeviceID
- CIM_VideoController.PowerManagementCapabilities
- CIM_VideoController.PowerManagementSupported
- CIM_VideoController.ProtocolSupported
- CIM_VideoController.Status
- CIM_VideoController.StatusInfo
- CIM_VideoController.SystemCreationClassName
- CIM_VideoController.SystemName
- CIM_VideoController.TimeOfLastReset
- CIM_VideoController.VideoMemoryType
- CIM_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6475c99e7a6f2ee1bef56bf2c266c788efc0b805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896297"
---
# <a name="cim_videocontroller-class"></a><span data-ttu-id="b608b-103">\_Класс CIM видеоконтроллер</span><span class="sxs-lookup"><span data-stu-id="b608b-103">CIM\_VideoController class</span></span>

<span data-ttu-id="b608b-104">Класс **CIM \_ Видеоконтроллер** представляет возможности и управление видеоконтроллером.</span><span class="sxs-lookup"><span data-stu-id="b608b-104">The **CIM\_VideoController** class represents the capabilities and management of the video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b608b-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b608b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b608b-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b608b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b608b-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b608b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b608b-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b608b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b608b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b608b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE5-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoController : CIM_Controller
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
  uint16   VideoMemoryType;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="b608b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="b608b-110">Members</span></span>

<span data-ttu-id="b608b-111">Класс **CIM \_ Видеоконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b608b-111">The **CIM\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="b608b-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b608b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b608b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b608b-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b608b-114">Методы</span><span class="sxs-lookup"><span data-stu-id="b608b-114">Methods</span></span>

<span data-ttu-id="b608b-115">Класс **CIM \_ Видеоконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b608b-115">The **CIM\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="b608b-116">Метод</span><span class="sxs-lookup"><span data-stu-id="b608b-116">Method</span></span>                                                                     | <span data-ttu-id="b608b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b608b-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b608b-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="b608b-118">**Reset**</span></span>](reset-method-in-class-cim-videocontroller.md)                 | <span data-ttu-id="b608b-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b608b-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="b608b-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b608b-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b608b-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b608b-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-videocontroller.md) | <span data-ttu-id="b608b-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="b608b-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b608b-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b608b-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b608b-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="b608b-124">Properties</span></span>

<span data-ttu-id="b608b-125">Класс **CIM \_ Видеоконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b608b-125">The **CIM\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b608b-126">**акцелераторкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="b608b-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-127">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="b608b-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b608b-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-129">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Видеоконтроллер**.**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="b608b-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-130">Графические и трехмерные возможности видеоконтроллера.</span><span class="sxs-lookup"><span data-stu-id="b608b-130">Graphics and 3-D capabilities of the video controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b608b-131">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b608b-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b608b-132">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b608b-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="b608b-133">**Графический ускоритель** (2)</span><span class="sxs-lookup"><span data-stu-id="b608b-133">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="b608b-134">**трехмерный ускоритель** (3)</span><span class="sxs-lookup"><span data-stu-id="b608b-134">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b608b-135">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="b608b-135">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-136">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b608b-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-138">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="b608b-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-139">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="b608b-139">Availability and status of the device.</span></span>

<span data-ttu-id="b608b-140">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-140">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b608b-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b608b-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b608b-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b608b-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b608b-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="b608b-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b608b-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="b608b-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b608b-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="b608b-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b608b-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="b608b-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b608b-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="b608b-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b608b-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="b608b-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b608b-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="b608b-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b608b-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="b608b-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b608b-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="b608b-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b608b-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="b608b-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b608b-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="b608b-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-154">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b608b-154">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b608b-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="b608b-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-156">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="b608b-156">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b608b-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="b608b-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-158">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="b608b-158">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b608b-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="b608b-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b608b-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="b608b-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-161">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b608b-161">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b608b-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="b608b-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-163">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="b608b-163">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b608b-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="b608b-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-165">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="b608b-165">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b608b-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="b608b-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-167">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="b608b-167">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b608b-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="b608b-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-169">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="b608b-169">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b608b-170">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="b608b-170">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-171">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="b608b-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b608b-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-173">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Видеоконтроллер**.**Акцелераторкапабилитиес**")</span><span class="sxs-lookup"><span data-stu-id="b608b-173">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-174">Строки произвольной формы, содержащие подробные описания функций ускорителя видео, указанных в массиве **акцелераторкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b608b-174">Free-form strings that provide detailed descriptions for the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="b608b-175">Каждая запись этого массива связана с записью в массиве **акцелераторкапабилитиес** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="b608b-175">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="b608b-176">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b608b-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b608b-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-179">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b608b-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-180">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b608b-180">Short textual description of the object.</span></span>

<span data-ttu-id="b608b-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b608b-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-182">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b608b-182">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-183">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-185">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b608b-185">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-186">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b608b-186">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b608b-187">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-187">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b608b-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="b608b-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b608b-189"> (0)</span><span class="sxs-lookup"><span data-stu-id="b608b-189">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-190">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="b608b-190">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b608b-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="b608b-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b608b-192">(1)</span><span class="sxs-lookup"><span data-stu-id="b608b-192">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-193">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="b608b-193">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b608b-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b608b-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b608b-195">(2)</span><span class="sxs-lookup"><span data-stu-id="b608b-195">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b608b-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="b608b-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b608b-197">(3)</span><span class="sxs-lookup"><span data-stu-id="b608b-197">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-198">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b608b-198">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b608b-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b608b-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b608b-200">(4)</span><span class="sxs-lookup"><span data-stu-id="b608b-200">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-201">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b608b-201">Device is not working properly.</span></span> <span data-ttu-id="b608b-202">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b608b-202">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b608b-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="b608b-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b608b-204">(5)</span><span class="sxs-lookup"><span data-stu-id="b608b-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-205">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="b608b-205">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b608b-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="b608b-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b608b-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="b608b-207">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-208">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="b608b-208">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b608b-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="b608b-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b608b-210">(7)</span><span class="sxs-lookup"><span data-stu-id="b608b-210">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b608b-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b608b-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b608b-212">(8)</span><span class="sxs-lookup"><span data-stu-id="b608b-212">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-213">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="b608b-213">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b608b-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b608b-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b608b-215">(9)</span><span class="sxs-lookup"><span data-stu-id="b608b-215">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-216">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b608b-216">Device is not working properly.</span></span> <span data-ttu-id="b608b-217">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="b608b-217">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b608b-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="b608b-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b608b-219">(10)</span><span class="sxs-lookup"><span data-stu-id="b608b-219">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-220">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="b608b-220">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b608b-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="b608b-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b608b-222">(11)</span><span class="sxs-lookup"><span data-stu-id="b608b-222">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-223">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="b608b-223">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b608b-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="b608b-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b608b-225">(12)</span><span class="sxs-lookup"><span data-stu-id="b608b-225">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-226">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="b608b-226">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b608b-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b608b-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b608b-228">(13)</span><span class="sxs-lookup"><span data-stu-id="b608b-228">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-229">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="b608b-229">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b608b-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="b608b-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b608b-231">(14)</span><span class="sxs-lookup"><span data-stu-id="b608b-231">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-232">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="b608b-232">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b608b-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="b608b-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b608b-234">(15)</span><span class="sxs-lookup"><span data-stu-id="b608b-234">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-235">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="b608b-235">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b608b-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b608b-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b608b-237">(16)</span><span class="sxs-lookup"><span data-stu-id="b608b-237">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-238">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="b608b-238">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b608b-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="b608b-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b608b-240">(17)</span><span class="sxs-lookup"><span data-stu-id="b608b-240">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-241">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="b608b-241">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b608b-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b608b-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b608b-243">(18)</span><span class="sxs-lookup"><span data-stu-id="b608b-243">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-244">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b608b-244">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b608b-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="b608b-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b608b-246">(19)</span><span class="sxs-lookup"><span data-stu-id="b608b-246">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b608b-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b608b-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b608b-248">(20)</span><span class="sxs-lookup"><span data-stu-id="b608b-248">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-249">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b608b-249">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b608b-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="b608b-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b608b-251">(21)</span><span class="sxs-lookup"><span data-stu-id="b608b-251">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-252">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b608b-252">System failure.</span></span> <span data-ttu-id="b608b-253">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b608b-253">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b608b-254">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="b608b-254">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b608b-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="b608b-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b608b-256">(22)</span><span class="sxs-lookup"><span data-stu-id="b608b-256">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-257">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b608b-257">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b608b-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="b608b-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b608b-259">(23)</span><span class="sxs-lookup"><span data-stu-id="b608b-259">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-260">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b608b-260">System failure.</span></span> <span data-ttu-id="b608b-261">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b608b-261">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b608b-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="b608b-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b608b-263">(24)</span><span class="sxs-lookup"><span data-stu-id="b608b-263">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-264">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="b608b-264">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b608b-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b608b-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b608b-266">(25)</span><span class="sxs-lookup"><span data-stu-id="b608b-266">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-267">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b608b-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b608b-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b608b-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b608b-269">(26)</span><span class="sxs-lookup"><span data-stu-id="b608b-269">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-270">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b608b-270">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b608b-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="b608b-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b608b-272">(27)</span><span class="sxs-lookup"><span data-stu-id="b608b-272">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-273">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="b608b-273">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b608b-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="b608b-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b608b-275">(28)</span><span class="sxs-lookup"><span data-stu-id="b608b-275">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-276">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="b608b-276">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b608b-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="b608b-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b608b-278">(29)</span><span class="sxs-lookup"><span data-stu-id="b608b-278">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-279">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b608b-279">Device is disabled.</span></span> <span data-ttu-id="b608b-280">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b608b-280">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b608b-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b608b-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b608b-282">(30)</span><span class="sxs-lookup"><span data-stu-id="b608b-282">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-283">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="b608b-283">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b608b-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b608b-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b608b-285">1-31</span><span class="sxs-lookup"><span data-stu-id="b608b-285">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-286">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b608b-286">Device is not working properly.</span></span> <span data-ttu-id="b608b-287">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b608b-287">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b608b-288">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="b608b-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-289">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b608b-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-291">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b608b-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-292">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b608b-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b608b-293">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-294">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b608b-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-295">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b608b-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-297">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b608b-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b608b-298">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b608b-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b608b-299">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="b608b-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b608b-300">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-301">**куррентбитсперпиксел**</span><span class="sxs-lookup"><span data-stu-id="b608b-301">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-302">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-304">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,12 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" BITS ")</span><span class="sxs-lookup"><span data-stu-id="b608b-304">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-305">Число битов, используемых для вывода каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="b608b-305">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="b608b-306">**курренсоризонталресолутион**</span><span class="sxs-lookup"><span data-stu-id="b608b-306">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-307">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-309">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")</span><span class="sxs-lookup"><span data-stu-id="b608b-309">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-310">Текущее число точек по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="b608b-310">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b608b-311">**куррентнумберофколорс**</span><span class="sxs-lookup"><span data-stu-id="b608b-311">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-312">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b608b-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b608b-314">Число цветов, поддерживаемое при текущем разрешении.</span><span class="sxs-lookup"><span data-stu-id="b608b-314">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="b608b-315">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b608b-315">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-316">**куррентнумберофколумнс**</span><span class="sxs-lookup"><span data-stu-id="b608b-316">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-317">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-319">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="b608b-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-320">Если в символьном режиме, число столбцов для видеоконтроллера; в противном случае введите 0.</span><span class="sxs-lookup"><span data-stu-id="b608b-320">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="b608b-321">**куррентнумберофровс**</span><span class="sxs-lookup"><span data-stu-id="b608b-321">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-322">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-324">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="b608b-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-325">Если в символьном режиме, число строк для видеоконтроллера; в противном случае введите 0.</span><span class="sxs-lookup"><span data-stu-id="b608b-325">If in character mode, number of rows for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="b608b-326">**куррентрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="b608b-326">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-327">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-329">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,15 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="b608b-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-330">Текущая частота обновления в герцах.</span><span class="sxs-lookup"><span data-stu-id="b608b-330">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="b608b-331">**куррентсканмоде**</span><span class="sxs-lookup"><span data-stu-id="b608b-331">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-332">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b608b-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-334">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="b608b-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-335">Текущий режим просмотра.</span><span class="sxs-lookup"><span data-stu-id="b608b-335">Current scan mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b608b-336">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b608b-336">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b608b-337">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b608b-337">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="b608b-338">С **чередованием** (3)</span><span class="sxs-lookup"><span data-stu-id="b608b-338">**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="b608b-339">**Без чередования** (4)</span><span class="sxs-lookup"><span data-stu-id="b608b-339">**Non Interlaced** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b608b-340">**куррентвертикалресолутион**</span><span class="sxs-lookup"><span data-stu-id="b608b-340">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-341">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-343">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,10 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")</span><span class="sxs-lookup"><span data-stu-id="b608b-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-344">Текущее число пикселей по вертикали.</span><span class="sxs-lookup"><span data-stu-id="b608b-344">Current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b608b-345">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b608b-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b608b-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-348">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="b608b-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-349">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b608b-349">Textual description of the object.</span></span>

<span data-ttu-id="b608b-350">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b608b-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b608b-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b608b-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-354">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b608b-354">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b608b-355">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b608b-355">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b608b-356">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-357">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="b608b-357">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-358">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b608b-358">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b608b-360">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="b608b-360">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b608b-361">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-362">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b608b-362">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-363">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b608b-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b608b-365">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="b608b-365">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b608b-366">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-367">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b608b-367">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-368">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b608b-368">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-370">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="b608b-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-371">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b608b-371">Date and time the object was installed.</span></span> <span data-ttu-id="b608b-372">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="b608b-372">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b608b-373">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b608b-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-374">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b608b-374">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-375">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b608b-377">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="b608b-377">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b608b-378">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-379">**максмеморисуппортед**</span><span class="sxs-lookup"><span data-stu-id="b608b-379">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-380">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-382">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="b608b-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-383">Максимальный поддерживаемый объем памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="b608b-383">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b608b-384">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="b608b-384">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-385">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-386">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-387">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="b608b-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-388">Максимальное количество напрямую обрабатываемых сущностей, поддерживаемых контроллером.</span><span class="sxs-lookup"><span data-stu-id="b608b-388">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="b608b-389">Если число неизвестно или неограниченно, следует использовать значение 0.</span><span class="sxs-lookup"><span data-stu-id="b608b-389">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="b608b-390">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="b608b-390">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-391">**максрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="b608b-391">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-392">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-394">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,5 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="b608b-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-395">Максимальная частота обновления контроллера видео в герцах.</span><span class="sxs-lookup"><span data-stu-id="b608b-395">Maximum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="b608b-396">**минрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="b608b-396">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-397">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-397">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-398">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-399">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,4 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="b608b-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-400">Минимальная частота обновления видеоконтроллера (в герцах).</span><span class="sxs-lookup"><span data-stu-id="b608b-400">Minimum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="b608b-401">**Name**</span><span class="sxs-lookup"><span data-stu-id="b608b-401">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-402">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b608b-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-404">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="b608b-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-405">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="b608b-405">Label by which the object is known.</span></span> <span data-ttu-id="b608b-406">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="b608b-406">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b608b-407">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b608b-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-408">**нумберофвидеопажес**</span><span class="sxs-lookup"><span data-stu-id="b608b-408">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-409">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b608b-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b608b-411">Количество поддерживаемых видео страниц с учетом текущих разрешений и доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="b608b-411">Number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="b608b-412">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b608b-412">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-413">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b608b-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-415">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b608b-415">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-416">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b608b-416">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b608b-417">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b608b-418">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b608b-418">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b608b-419">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="b608b-419">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-420">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="b608b-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b608b-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b608b-422">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="b608b-422">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b608b-423">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-423">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b608b-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b608b-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b608b-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="b608b-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b608b-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="b608b-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b608b-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b608b-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-428">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="b608b-428">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b608b-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="b608b-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-430">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="b608b-430">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b608b-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="b608b-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-432">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b608b-432">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b608b-433">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="b608b-433">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b608b-434">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b608b-434">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b608b-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="b608b-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-436">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="b608b-436">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b608b-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="b608b-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b608b-438">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="b608b-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b608b-439">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="b608b-439">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-440">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b608b-440">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b608b-442">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b608b-442">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b608b-443">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b608b-443">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b608b-444">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b608b-444">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b608b-445">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b608b-445">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b608b-446">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-447">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="b608b-447">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-448">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b608b-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-449">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-450">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b608b-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-451">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="b608b-451">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="b608b-452">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="b608b-452">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="b608b-453">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b608b-453">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b608b-454">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b608b-454">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b608b-455">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b608b-455">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="b608b-456">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="b608b-456">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="b608b-457">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="b608b-457">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="b608b-458">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="b608b-458">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="b608b-459">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="b608b-459">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="b608b-460">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="b608b-460">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="b608b-461">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="b608b-461">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="b608b-462">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="b608b-462">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="b608b-463">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="b608b-463">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="b608b-464">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="b608b-464">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="b608b-465">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="b608b-465">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="b608b-466">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="b608b-466">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="b608b-467">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="b608b-467">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="b608b-468">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="b608b-468">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="b608b-469">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="b608b-469">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="b608b-470">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="b608b-470">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="b608b-471">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="b608b-471">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="b608b-472">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="b608b-472">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="b608b-473">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="b608b-473">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="b608b-474">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="b608b-474">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="b608b-475">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="b608b-475">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="b608b-476">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="b608b-476">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="b608b-477">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="b608b-477">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="b608b-478">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="b608b-478">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="b608b-479">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="b608b-479">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="b608b-480">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="b608b-480">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="b608b-481">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="b608b-481">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="b608b-482">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="b608b-482">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="b608b-483">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="b608b-483">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="b608b-484">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="b608b-484">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="b608b-485">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="b608b-485">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="b608b-486">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="b608b-486">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="b608b-487">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="b608b-487">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="b608b-488">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="b608b-488">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="b608b-489">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="b608b-489">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="b608b-490">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="b608b-490">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="b608b-491">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="b608b-491">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="b608b-492">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="b608b-492">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="b608b-493">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="b608b-493">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="b608b-494">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="b608b-494">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="b608b-495">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="b608b-495">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="b608b-496">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="b608b-496">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="b608b-497">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="b608b-497">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="b608b-498">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="b608b-498">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="b608b-499">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="b608b-499">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="b608b-500">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="b608b-500">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b608b-501">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b608b-501">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-502">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b608b-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-503">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-504">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="b608b-504">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-505">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b608b-505">Current status of the object.</span></span> <span data-ttu-id="b608b-506">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b608b-506">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b608b-507">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="b608b-507">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b608b-508">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="b608b-508">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b608b-509">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="b608b-509">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b608b-510">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="b608b-510">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b608b-511">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b608b-511">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b608b-512">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b608b-512">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b608b-513">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b608b-513">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b608b-514">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="b608b-514">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b608b-515">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="b608b-515">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b608b-516">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="b608b-516">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b608b-517">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="b608b-517">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b608b-518">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="b608b-518">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b608b-519">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="b608b-519">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b608b-520">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b608b-520">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-521">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b608b-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-522">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-523">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b608b-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-524">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b608b-524">State of the logical device.</span></span> <span data-ttu-id="b608b-525">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="b608b-525">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b608b-526">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-526">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b608b-527">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b608b-527">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b608b-528">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b608b-528">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b608b-529">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b608b-529">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b608b-530">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="b608b-530">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b608b-531">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="b608b-531">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b608b-532">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="b608b-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-533">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b608b-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-534">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-535">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b608b-535">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b608b-536">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="b608b-536">Scoping system's creation class name.</span></span>

<span data-ttu-id="b608b-537">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-537">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-538">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b608b-538">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-539">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b608b-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-540">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-541">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b608b-541">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b608b-542">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="b608b-542">Scoping system's name.</span></span>

<span data-ttu-id="b608b-543">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b608b-543">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-544">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="b608b-544">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-545">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b608b-545">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-546">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-546">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b608b-547">Дата и время последнего сброса контроллера, означающее, что контроллер был отключен или инициализирован повторно.</span><span class="sxs-lookup"><span data-stu-id="b608b-547">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="b608b-548">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="b608b-548">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="b608b-549">**видеомеморитипе**</span><span class="sxs-lookup"><span data-stu-id="b608b-549">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-550">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b608b-550">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-551">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b608b-552">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="b608b-552">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="b608b-553">Тип видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="b608b-553">Type of video memory.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b608b-554">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b608b-554">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b608b-555">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b608b-555">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="b608b-556">**Видеопамять** (3)</span><span class="sxs-lookup"><span data-stu-id="b608b-556">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="b608b-557">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="b608b-557">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="b608b-558">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="b608b-558">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="b608b-559">**Врам** (6)</span><span class="sxs-lookup"><span data-stu-id="b608b-559">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="b608b-560">**ОЗУ Эдо** (7)</span><span class="sxs-lookup"><span data-stu-id="b608b-560">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="b608b-561">**Пакетная синхронная DRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="b608b-561">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="b608b-562">**Конвейерный пакет SRAM** (9)</span><span class="sxs-lookup"><span data-stu-id="b608b-562">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="b608b-563">**Кдрам** (10)</span><span class="sxs-lookup"><span data-stu-id="b608b-563">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="b608b-564">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="b608b-564">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="b608b-565">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="b608b-565">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="b608b-566">**Сграм** (13)</span><span class="sxs-lookup"><span data-stu-id="b608b-566">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b608b-567">**видеопроцессор**</span><span class="sxs-lookup"><span data-stu-id="b608b-567">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b608b-568">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b608b-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b608b-569">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b608b-569">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b608b-570">Произвольная строка, описывающая обработчик видео или контроллер.</span><span class="sxs-lookup"><span data-stu-id="b608b-570">Free-form string that describes the video processor or controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b608b-571">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b608b-571">Remarks</span></span>

<span data-ttu-id="b608b-572">Класс **CIM \_ Видеоконтроллер** является производным от [**\_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="b608b-572">The **CIM\_VideoController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="b608b-573">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="b608b-573">WMI does not implement this class.</span></span> <span data-ttu-id="b608b-574">Классы WMI, производные от **CIM \_ Видеоконтроллер**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b608b-574">For WMI classes derived from **CIM\_VideoController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b608b-575">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b608b-575">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b608b-576">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b608b-576">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b608b-577">Требования</span><span class="sxs-lookup"><span data-stu-id="b608b-577">Requirements</span></span>



| <span data-ttu-id="b608b-578">Требование</span><span class="sxs-lookup"><span data-stu-id="b608b-578">Requirement</span></span> | <span data-ttu-id="b608b-579">Значение</span><span class="sxs-lookup"><span data-stu-id="b608b-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b608b-580">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b608b-580">Minimum supported client</span></span><br/> | <span data-ttu-id="b608b-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b608b-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b608b-582">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b608b-582">Minimum supported server</span></span><br/> | <span data-ttu-id="b608b-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b608b-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b608b-584">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b608b-584">Namespace</span></span><br/>                | <span data-ttu-id="b608b-585">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b608b-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b608b-586">MOF</span><span class="sxs-lookup"><span data-stu-id="b608b-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b608b-587"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b608b-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b608b-588">DLL</span><span class="sxs-lookup"><span data-stu-id="b608b-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b608b-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b608b-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b608b-590">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b608b-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b608b-591">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="b608b-591">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

