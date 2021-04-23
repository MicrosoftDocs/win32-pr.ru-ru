---
description: Представляет возможности и емкость управления видеоконтроллером в компьютерной системе под управлением Windows.
ms.assetid: 5c81994b-4a84-46ff-8689-09998dc66f91
ms.tgt_platform: multiple
title: Класс Win32_VideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoController
- Win32_VideoController.Reset
- Win32_VideoController.SetPowerState
- Win32_VideoController.AcceleratorCapabilities
- Win32_VideoController.AdapterCompatibility
- Win32_VideoController.AdapterDACType
- Win32_VideoController.AdapterRAM
- Win32_VideoController.Availability
- Win32_VideoController.CapabilityDescriptions
- Win32_VideoController.Caption
- Win32_VideoController.ColorTableEntries
- Win32_VideoController.ConfigManagerErrorCode
- Win32_VideoController.ConfigManagerUserConfig
- Win32_VideoController.CreationClassName
- Win32_VideoController.CurrentBitsPerPixel
- Win32_VideoController.CurrentHorizontalResolution
- Win32_VideoController.CurrentNumberOfColors
- Win32_VideoController.CurrentNumberOfColumns
- Win32_VideoController.CurrentNumberOfRows
- Win32_VideoController.CurrentRefreshRate
- Win32_VideoController.CurrentScanMode
- Win32_VideoController.CurrentVerticalResolution
- Win32_VideoController.Description
- Win32_VideoController.DeviceID
- Win32_VideoController.DeviceSpecificPens
- Win32_VideoController.DitherType
- Win32_VideoController.DriverDate
- Win32_VideoController.DriverVersion
- Win32_VideoController.ErrorCleared
- Win32_VideoController.ErrorDescription
- Win32_VideoController.ICMIntent
- Win32_VideoController.ICMMethod
- Win32_VideoController.InfFilename
- Win32_VideoController.InfSection
- Win32_VideoController.InstallDate
- Win32_VideoController.InstalledDisplayDrivers
- Win32_VideoController.LastErrorCode
- Win32_VideoController.MaxMemorySupported
- Win32_VideoController.MaxNumberControlled
- Win32_VideoController.MaxRefreshRate
- Win32_VideoController.MinRefreshRate
- Win32_VideoController.Monochrome
- Win32_VideoController.Name
- Win32_VideoController.NumberOfColorPlanes
- Win32_VideoController.NumberOfVideoPages
- Win32_VideoController.PNPDeviceID
- Win32_VideoController.PowerManagementCapabilities
- Win32_VideoController.PowerManagementSupported
- Win32_VideoController.ProtocolSupported
- Win32_VideoController.ReservedSystemPaletteEntries
- Win32_VideoController.SpecificationVersion
- Win32_VideoController.Status
- Win32_VideoController.StatusInfo
- Win32_VideoController.SystemCreationClassName
- Win32_VideoController.SystemName
- Win32_VideoController.SystemPaletteEntries
- Win32_VideoController.TimeOfLastReset
- Win32_VideoController.VideoArchitecture
- Win32_VideoController.VideoMemoryType
- Win32_VideoController.VideoMode
- Win32_VideoController.VideoModeDescription
- Win32_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deb6903ba6cf27170539281da90569a14471999c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495831"
---
# <a name="win32_videocontroller-class"></a><span data-ttu-id="dd17b-103">\_Класс Win32 видеоконтроллер</span><span class="sxs-lookup"><span data-stu-id="dd17b-103">Win32\_VideoController class</span></span>

<span data-ttu-id="dd17b-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ Видеоконтроллер для Win32** представляет возможности и Управление емкостью видеоконтроллера в компьютерной системе под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="dd17b-104">The **Win32\_VideoController** [WMI class](../wmisdk/retrieving-a-class.md) represents the capabilities and management capacity of the video controller on a computer system running Windows.</span></span>

<span data-ttu-id="dd17b-105">Оборудование, несовместимое с моделью драйвера Windows (WDDM), возвращает неточные значения свойств для экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="dd17b-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="dd17b-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="dd17b-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dd17b-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="dd17b-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd17b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd17b-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF1-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoController : CIM_PCVideoController
{
  uint16   AcceleratorCapabilities[];
  string   AdapterCompatibility;
  string   AdapterDACType;
  uint32   AdapterRAM;
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ColorTableEntries;
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
  uint32   DeviceSpecificPens;
  uint32   DitherType;
  datetime DriverDate;
  string   DriverVersion;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   ICMIntent;
  uint32   ICMMethod;
  string   InfFilename;
  string   InfSection;
  datetime InstallDate;
  string   InstalledDisplayDrivers;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  boolean  Monochrome;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  uint32   ReservedSystemPaletteEntries;
  uint32   SpecificationVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   SystemPaletteEntries;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoModeDescription;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="dd17b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="dd17b-109">Members</span></span>

<span data-ttu-id="dd17b-110">Класс **Win32 \_ Видеоконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dd17b-110">The **Win32\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="dd17b-111">Методы</span><span class="sxs-lookup"><span data-stu-id="dd17b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd17b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd17b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd17b-113">Методы</span><span class="sxs-lookup"><span data-stu-id="dd17b-113">Methods</span></span>

<span data-ttu-id="dd17b-114">Класс **Win32 \_ Видеоконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dd17b-114">The **Win32\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="dd17b-115">Метод</span><span class="sxs-lookup"><span data-stu-id="dd17b-115">Method</span></span>            | <span data-ttu-id="dd17b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="dd17b-116">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd17b-117">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="dd17b-117">**Reset**</span></span>         | <span data-ttu-id="dd17b-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="dd17b-118">Not implemented.</span></span> <span data-ttu-id="dd17b-119">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ пквидеоконтроллер**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/>                 |
| <span data-ttu-id="dd17b-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dd17b-120">**SetPowerState**</span></span> | <span data-ttu-id="dd17b-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="dd17b-121">Not implemented.</span></span> <span data-ttu-id="dd17b-122">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ пквидеоконтроллер**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dd17b-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd17b-123">Properties</span></span>

<span data-ttu-id="dd17b-124">Класс **Win32 \_ Видеоконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dd17b-124">The **Win32\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd17b-125">**акцелераторкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="dd17b-125">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-126">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dd17b-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-128">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="dd17b-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-129">Массив графических и трехмерных возможностей видеоконтроллера.</span><span class="sxs-lookup"><span data-stu-id="dd17b-129">Array of graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="dd17b-130">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-130">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd17b-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dd17b-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd17b-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="dd17b-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Графический ускоритель** (2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="dd17b-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**трехмерный ускоритель** (3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-135">трехмерный ускоритель</span><span class="sxs-lookup"><span data-stu-id="dd17b-135">3-D Accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-136">**адаптеркомпатибилити**</span><span class="sxs-lookup"><span data-stu-id="dd17b-136">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-139">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="dd17b-139">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-140">Общий набор микросхем, используемый этим контроллером для сравнения совместимости с системой.</span><span class="sxs-lookup"><span data-stu-id="dd17b-140">General chipset used for this controller to compare compatibilities with the system.</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-141">**адаптердактипе**</span><span class="sxs-lookup"><span data-stu-id="dd17b-141">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-144">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| хардвареинформатион. DACType")</span><span class="sxs-lookup"><span data-stu-id="dd17b-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.DACType")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-145">Имя или идентификатор микросхемы цифрового преобразования (DAC).</span><span class="sxs-lookup"><span data-stu-id="dd17b-145">Name or identifier of the digital-to-analog converter (DAC) chip.</span></span> <span data-ttu-id="dd17b-146">Кодировка этого свойства — буквенно-цифровая.</span><span class="sxs-lookup"><span data-stu-id="dd17b-146">The character set of this property is alphanumeric.</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-147">**адаптеррам**</span><span class="sxs-lookup"><span data-stu-id="dd17b-147">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-148">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-150">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| хардвареинформатион. MemorySize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="dd17b-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.MemorySize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-151">Объем памяти видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="dd17b-151">Memory size of the video adapter.</span></span>

<span data-ttu-id="dd17b-152">Пример: 64000</span><span class="sxs-lookup"><span data-stu-id="dd17b-152">Example: 64000</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-153">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="dd17b-153">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-154">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd17b-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-156">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-157">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="dd17b-157">Availability and status of the device.</span></span>

<span data-ttu-id="dd17b-158">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-158">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd17b-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd17b-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="dd17b-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-162">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="dd17b-162">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dd17b-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="dd17b-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="dd17b-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="dd17b-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dd17b-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="dd17b-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dd17b-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="dd17b-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="dd17b-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="dd17b-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-168">Автономная миграция</span><span class="sxs-lookup"><span data-stu-id="dd17b-168">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="dd17b-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="dd17b-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dd17b-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="dd17b-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="dd17b-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="dd17b-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="dd17b-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="dd17b-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="dd17b-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="dd17b-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-174">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="dd17b-174">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dd17b-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="dd17b-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-176">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="dd17b-176">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dd17b-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="dd17b-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-178">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="dd17b-178">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dd17b-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="dd17b-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="dd17b-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="dd17b-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-181">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="dd17b-181">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dd17b-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="dd17b-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-183">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="dd17b-183">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="dd17b-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="dd17b-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-185">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="dd17b-185">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="dd17b-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="dd17b-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-187">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="dd17b-187">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="dd17b-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="dd17b-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-189">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="dd17b-189">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-190">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="dd17b-190">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-191">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dd17b-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-193">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Акцелераторкапабилитиес**")</span><span class="sxs-lookup"><span data-stu-id="dd17b-193">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-194">Строки произвольной формы, предоставляющие более подробные объяснения для любого из функций ускорителя видео, указанных в массиве **акцелераторкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="dd17b-194">Free-form strings providing more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="dd17b-195">Обратите внимание, что каждая запись этого массива связана с записью в массиве **акцелераторкапабилитиес** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="dd17b-195">Note, each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

<span data-ttu-id="dd17b-196">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-196">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-197">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="dd17b-197">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-200">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dd17b-200">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-201">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dd17b-201">Short description of the object.</span></span>

<span data-ttu-id="dd17b-202">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-202">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-203">**колортаблинтриес**</span><span class="sxs-lookup"><span data-stu-id="dd17b-203">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-204">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-206">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="dd17b-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-207">Размер таблицы цветов системы.</span><span class="sxs-lookup"><span data-stu-id="dd17b-207">Size of the system's color table.</span></span> <span data-ttu-id="dd17b-208">Устройство должно иметь глубину цвета не более 8 бит на пиксель; в противном случае это свойство не задано.</span><span class="sxs-lookup"><span data-stu-id="dd17b-208">The device must have a color depth of no more than 8 bits per pixel; otherwise, this property is not set.</span></span>

<span data-ttu-id="dd17b-209">Пример: 256</span><span class="sxs-lookup"><span data-stu-id="dd17b-209">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-210">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="dd17b-210">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-211">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-213">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dd17b-213">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-214">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="dd17b-214">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="dd17b-215">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-215">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="dd17b-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="dd17b-217"> (0)</span><span class="sxs-lookup"><span data-stu-id="dd17b-217">(0)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-218">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="dd17b-218">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="dd17b-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="dd17b-220">(1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-220">(1)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-221">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="dd17b-221">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dd17b-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="dd17b-223">(2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-223">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="dd17b-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="dd17b-225">(3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-225">(3)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-226">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd17b-226">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dd17b-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="dd17b-228">(4)</span><span class="sxs-lookup"><span data-stu-id="dd17b-228">(4)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-229">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="dd17b-229">Device is not working properly.</span></span> <span data-ttu-id="dd17b-230">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="dd17b-230">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="dd17b-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="dd17b-232">(5)</span><span class="sxs-lookup"><span data-stu-id="dd17b-232">(5)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-233">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="dd17b-233">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="dd17b-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="dd17b-235"> (6)</span><span class="sxs-lookup"><span data-stu-id="dd17b-235">(6)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-236">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="dd17b-236">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="dd17b-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="dd17b-238">(7)</span><span class="sxs-lookup"><span data-stu-id="dd17b-238">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="dd17b-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="dd17b-240">(8)</span><span class="sxs-lookup"><span data-stu-id="dd17b-240">(8)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-241">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="dd17b-241">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="dd17b-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="dd17b-243">(9)</span><span class="sxs-lookup"><span data-stu-id="dd17b-243">(9)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-244">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="dd17b-244">Device is not working properly.</span></span> <span data-ttu-id="dd17b-245">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="dd17b-245">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="dd17b-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="dd17b-247">(10)</span><span class="sxs-lookup"><span data-stu-id="dd17b-247">(10)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-248">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="dd17b-248">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="dd17b-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="dd17b-250">(11)</span><span class="sxs-lookup"><span data-stu-id="dd17b-250">(11)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-251">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="dd17b-251">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="dd17b-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="dd17b-253">(12)</span><span class="sxs-lookup"><span data-stu-id="dd17b-253">(12)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-254">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="dd17b-254">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="dd17b-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="dd17b-256">(13)</span><span class="sxs-lookup"><span data-stu-id="dd17b-256">(13)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-257">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="dd17b-257">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="dd17b-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="dd17b-259">(14)</span><span class="sxs-lookup"><span data-stu-id="dd17b-259">(14)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-260">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="dd17b-260">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="dd17b-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="dd17b-262">(15)</span><span class="sxs-lookup"><span data-stu-id="dd17b-262">(15)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-263">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="dd17b-263">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="dd17b-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="dd17b-265">(16)</span><span class="sxs-lookup"><span data-stu-id="dd17b-265">(16)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-266">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="dd17b-266">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="dd17b-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="dd17b-268">(17)</span><span class="sxs-lookup"><span data-stu-id="dd17b-268">(17)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-269">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd17b-269">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dd17b-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="dd17b-271">(18)</span><span class="sxs-lookup"><span data-stu-id="dd17b-271">(18)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-272">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="dd17b-272">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="dd17b-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="dd17b-274">(19)</span><span class="sxs-lookup"><span data-stu-id="dd17b-274">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dd17b-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="dd17b-276">(20)</span><span class="sxs-lookup"><span data-stu-id="dd17b-276">(20)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-277">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="dd17b-277">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="dd17b-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="dd17b-279">(21)</span><span class="sxs-lookup"><span data-stu-id="dd17b-279">(21)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-280">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="dd17b-280">System failure.</span></span> <span data-ttu-id="dd17b-281">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="dd17b-281">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="dd17b-282">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="dd17b-282">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="dd17b-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="dd17b-284">(22)</span><span class="sxs-lookup"><span data-stu-id="dd17b-284">(22)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-285">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="dd17b-285">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="dd17b-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="dd17b-287">(23)</span><span class="sxs-lookup"><span data-stu-id="dd17b-287">(23)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-288">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="dd17b-288">System failure.</span></span> <span data-ttu-id="dd17b-289">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="dd17b-289">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="dd17b-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="dd17b-291">(24)</span><span class="sxs-lookup"><span data-stu-id="dd17b-291">(24)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-292">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="dd17b-292">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dd17b-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dd17b-294">(25)</span><span class="sxs-lookup"><span data-stu-id="dd17b-294">(25)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-295">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="dd17b-295">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dd17b-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dd17b-297">(26)</span><span class="sxs-lookup"><span data-stu-id="dd17b-297">(26)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-298">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="dd17b-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="dd17b-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="dd17b-300">(27)</span><span class="sxs-lookup"><span data-stu-id="dd17b-300">(27)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-301">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="dd17b-301">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="dd17b-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="dd17b-303">(28)</span><span class="sxs-lookup"><span data-stu-id="dd17b-303">(28)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-304">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="dd17b-304">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="dd17b-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="dd17b-306">(29)</span><span class="sxs-lookup"><span data-stu-id="dd17b-306">(29)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-307">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="dd17b-307">Device is disabled.</span></span> <span data-ttu-id="dd17b-308">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="dd17b-308">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="dd17b-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="dd17b-310">(30)</span><span class="sxs-lookup"><span data-stu-id="dd17b-310">(30)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-311">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="dd17b-311">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dd17b-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dd17b-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="dd17b-313">1-31</span><span class="sxs-lookup"><span data-stu-id="dd17b-313">(31)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-314">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="dd17b-314">Device is not working properly.</span></span> <span data-ttu-id="dd17b-315">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="dd17b-315">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-316">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="dd17b-316">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-317">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dd17b-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-319">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dd17b-319">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-320">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="dd17b-320">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="dd17b-321">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-322">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dd17b-322">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-323">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-325">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dd17b-325">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-326">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dd17b-326">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="dd17b-327">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="dd17b-327">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dd17b-328">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-329">**куррентбитсперпиксел**</span><span class="sxs-lookup"><span data-stu-id="dd17b-329">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-330">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-332">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Video \| 003,12 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" BITS ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-333">Число битов, используемых для вывода каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="dd17b-333">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="dd17b-334">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-334">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-335">**курренсоризонталресолутион**</span><span class="sxs-lookup"><span data-stu-id="dd17b-335">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-336">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-338">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Video \| 003,11 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" пикселей ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-339">Текущее число точек по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="dd17b-339">Current number of horizontal pixels.</span></span>

<span data-ttu-id="dd17b-340">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-340">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-341">**куррентнумберофколорс**</span><span class="sxs-lookup"><span data-stu-id="dd17b-341">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-342">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd17b-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-344">Число цветов, поддерживаемое при текущем разрешении.</span><span class="sxs-lookup"><span data-stu-id="dd17b-344">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="dd17b-345">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-345">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="dd17b-346">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-346">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-347">**куррентнумберофколумнс**</span><span class="sxs-lookup"><span data-stu-id="dd17b-347">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-348">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-350">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Video \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-351">Число столбцов для этого видеоконтроллера (в символьном режиме).</span><span class="sxs-lookup"><span data-stu-id="dd17b-351">Number of columns for this video controller (if in character mode).</span></span> <span data-ttu-id="dd17b-352">В противном случае введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="dd17b-352">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="dd17b-353">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-353">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-354">**куррентнумберофровс**</span><span class="sxs-lookup"><span data-stu-id="dd17b-354">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-355">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-357">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Video \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-358">Число строк для этого видеоконтроллера (в символьном режиме).</span><span class="sxs-lookup"><span data-stu-id="dd17b-358">Number of rows for this video controller (if in character mode).</span></span> <span data-ttu-id="dd17b-359">В противном случае введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="dd17b-359">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="dd17b-360">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-360">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-361">**куррентрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="dd17b-361">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-362">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-364">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("куррентрефрешрате"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Хардвареинформатион."), [**Units**](../wmisdk/standard-qualifiers.md) ("Герц")</span><span class="sxs-lookup"><span data-stu-id="dd17b-364">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation."), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-365">Частота, с которой видеоконтроллер обновляет изображение для монитора.</span><span class="sxs-lookup"><span data-stu-id="dd17b-365">Frequency at which the video controller refreshes the image for the monitor.</span></span> <span data-ttu-id="dd17b-366">Значение 0 (ноль) указывает, что используется скорость по умолчанию, а 0xFFFFFFFF указывает, что используется оптимальная скорость.</span><span class="sxs-lookup"><span data-stu-id="dd17b-366">A value of 0 (zero) indicates the default rate is being used, while 0xFFFFFFFF indicates the optimal rate is being used.</span></span>

<span data-ttu-id="dd17b-367">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-367">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-368">**куррентсканмоде**</span><span class="sxs-lookup"><span data-stu-id="dd17b-368">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-369">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd17b-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-371">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Video \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-372">Текущий режим просмотра.</span><span class="sxs-lookup"><span data-stu-id="dd17b-372">Current scan mode.</span></span>

<span data-ttu-id="dd17b-373">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-373">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd17b-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd17b-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="dd17b-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>С **чередованием** (3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="dd17b-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Без чередования** (4)</span><span class="sxs-lookup"><span data-stu-id="dd17b-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-378">Не с чередованием</span><span class="sxs-lookup"><span data-stu-id="dd17b-378">Noninterlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-379">**куррентвертикалресолутион**</span><span class="sxs-lookup"><span data-stu-id="dd17b-379">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-380">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-382">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Video \| 003,10 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" пикселей ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-383">Текущее число пикселей по вертикали.</span><span class="sxs-lookup"><span data-stu-id="dd17b-383">Current number of vertical pixels.</span></span>

<span data-ttu-id="dd17b-384">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-384">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-385">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dd17b-385">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-386">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-388">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="dd17b-388">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-389">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dd17b-389">Description of the object.</span></span>

<span data-ttu-id="dd17b-390">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-390">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-391">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dd17b-391">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-392">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-394">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dd17b-394">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-395">Идентификатор (уникальный для компьютерной системы) для этого видеоконтроллера.</span><span class="sxs-lookup"><span data-stu-id="dd17b-395">Identifier (unique to the computer system) for this video controller.</span></span>

<span data-ttu-id="dd17b-396">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-397">**девицеспеЦификпенс**</span><span class="sxs-lookup"><span data-stu-id="dd17b-397">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-398">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-400">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="dd17b-400">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-401">Текущее число перьев, зависящих от устройства.</span><span class="sxs-lookup"><span data-stu-id="dd17b-401">Current number of device-specific pens.</span></span> <span data-ttu-id="dd17b-402">Значение 0xFFFF означает, что устройство не поддерживает перья.</span><span class="sxs-lookup"><span data-stu-id="dd17b-402">A value of 0xffff means that the device does not support pens.</span></span>

<span data-ttu-id="dd17b-403">Пример: 3</span><span class="sxs-lookup"><span data-stu-id="dd17b-403">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-404">**дисертипе**</span><span class="sxs-lookup"><span data-stu-id="dd17b-404">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-405">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-407">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| енумдисплайсеттингс")</span><span class="sxs-lookup"><span data-stu-id="dd17b-407">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|EnumDisplaySettings")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-408">Тип изображения видеоконтроллера.</span><span class="sxs-lookup"><span data-stu-id="dd17b-408">Dither type of the video controller.</span></span> <span data-ttu-id="dd17b-409">Свойство может иметь одно из стандартных значений или определенное драйвером значение, которое больше или равно 256.</span><span class="sxs-lookup"><span data-stu-id="dd17b-409">The property can be one of the predefined values, or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="dd17b-410">Если выбрано смешение линий, контроллер использует метод сглаживания, который создает четко определенные границы между черным, белым и серым масштабированием.</span><span class="sxs-lookup"><span data-stu-id="dd17b-410">If line art dithering is chosen, the controller uses a dithering method that produces well-defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="dd17b-411">Цветовой дизеринг не подходит для изображений, которые содержат непрерывные оттенки интенсивности и тона, такие как отсканированные фотографии.</span><span class="sxs-lookup"><span data-stu-id="dd17b-411">Line art dithering is not suitable for images that include continuous graduations in intensity and hue such as scanned photographs.</span></span>

<dt>

<span id="No_dithering"></span><span id="no_dithering"></span><span id="NO_DITHERING"></span>

<span data-ttu-id="dd17b-412">**Без сглаживания** (1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-412">**No dithering** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_coarse_brush"></span><span id="dithering_with_a_coarse_brush"></span><span id="DITHERING_WITH_A_COARSE_BRUSH"></span>

<span data-ttu-id="dd17b-413">**Дизеринг с грубой кистью** (2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-413">**Dithering with a coarse brush** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_fine_brush"></span><span id="dithering_with_a_fine_brush"></span><span id="DITHERING_WITH_A_FINE_BRUSH"></span>

<span data-ttu-id="dd17b-414">**Сглаживание с помощью тонкой кисти** (3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-414">**Dithering with a fine brush** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_art_dithering"></span><span id="line_art_dithering"></span><span id="LINE_ART_DITHERING"></span>

<span data-ttu-id="dd17b-415">**Дизеринг линий** (4)</span><span class="sxs-lookup"><span data-stu-id="dd17b-415">**Line art dithering** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_does_gray_scaling"></span><span id="device_does_gray_scaling"></span><span id="DEVICE_DOES_GRAY_SCALING"></span>

<span data-ttu-id="dd17b-416">**Устройство имеет серый масштаб** (5)</span><span class="sxs-lookup"><span data-stu-id="dd17b-416">**Device does gray scaling** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-417">**дривердате**</span><span class="sxs-lookup"><span data-stu-id="dd17b-417">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-418">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dd17b-418">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-420">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| класс Win32Registry System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-420">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-421">Дата и время последнего изменения текущего установленного видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="dd17b-421">Last modification date and time of the currently installed video driver.</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-422">**дриверверсион**</span><span class="sxs-lookup"><span data-stu-id="dd17b-422">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-423">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-424">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-425">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| функции библиотеки установки файлов Win32API \| GetFileVersionInfo")</span><span class="sxs-lookup"><span data-stu-id="dd17b-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Installation Library Functions\|GetFileVersionInfo")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-426">Номер версии видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="dd17b-426">Version number of the video driver.</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-427">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="dd17b-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-428">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dd17b-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-430">Если **значение — true**, то ошибка, сообщаемая в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="dd17b-430">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="dd17b-431">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-432">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dd17b-432">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-433">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-434">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-435">Произвольная строка, предоставляя дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="dd17b-435">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="dd17b-436">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-437">**икминтент**</span><span class="sxs-lookup"><span data-stu-id="dd17b-437">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-438">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-439">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-440">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Printing spool Structures \| \| дмикминтент")</span><span class="sxs-lookup"><span data-stu-id="dd17b-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMIntent")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-441">Определенное значение одного из трех возможных методов сопоставления цветов или целей, которые должны использоваться по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dd17b-441">Specific value of one of the three possible color-matching methods or intents that should be used by default.</span></span> <span data-ttu-id="dd17b-442">Это свойство используется в основном для приложений, не поддерживающих ICM.</span><span class="sxs-lookup"><span data-stu-id="dd17b-442">This property is used primarily for non-ICM applications.</span></span> <span data-ttu-id="dd17b-443">ICM приложения устанавливают намерения, используя функции ICM.</span><span class="sxs-lookup"><span data-stu-id="dd17b-443">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="dd17b-444">Это свойство может быть стандартным значением или заданным драйвером, которое больше или равно 256.</span><span class="sxs-lookup"><span data-stu-id="dd17b-444">This property can be a predefined value or a driver defined value greater than or equal to 256.</span></span> <span data-ttu-id="dd17b-445">Сопоставление цветов на основе насыщенности — наиболее подходящий вариант для бизнес-графиков, когда нежелательно сглаживание.</span><span class="sxs-lookup"><span data-stu-id="dd17b-445">Color matching based on saturation is the most appropriate choice for business graphs when dithering is not desired.</span></span> <span data-ttu-id="dd17b-446">Сопоставление цветов на основе контрастности — наиболее подходящий вариант для отсканированных или фотографических изображений при необходимости сглаживания.</span><span class="sxs-lookup"><span data-stu-id="dd17b-446">Color matching based on contrast is the most appropriate choice for scanned or photographic images when dithering is desired.</span></span> <span data-ttu-id="dd17b-447">Цвет, оптимизированный для точного соответствия требуемому цвету, наиболее подходит для использования с деловыми логотипами или другими изображениями при необходимости точного соответствия цветов.</span><span class="sxs-lookup"><span data-stu-id="dd17b-447">Color matching optimized to match the exact color requested is most appropriate for use with business logos or other images when an exact color match is desired.</span></span>

<dt>

<span id="Saturation"></span><span id="saturation"></span><span id="SATURATION"></span>

<span data-ttu-id="dd17b-448">**Насыщенность** (1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-448">**Saturation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Contrast"></span><span id="contrast"></span><span id="CONTRAST"></span>

<span data-ttu-id="dd17b-449">**Контрастность** (2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-449">**Contrast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Exact_Color"></span><span id="exact_color"></span><span id="EXACT_COLOR"></span>

<span data-ttu-id="dd17b-450">**Точный цвет** (3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-450">**Exact Color** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-451">**икммесод**</span><span class="sxs-lookup"><span data-stu-id="dd17b-451">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-452">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-454">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Printing spool Structures \| \| дмикммесод")</span><span class="sxs-lookup"><span data-stu-id="dd17b-454">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMMethod")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-455">Метод обработки ICM.</span><span class="sxs-lookup"><span data-stu-id="dd17b-455">Method of handling ICM.</span></span> <span data-ttu-id="dd17b-456">Для приложений, не использующих ICM, это свойство определяет, включен ли ICM.</span><span class="sxs-lookup"><span data-stu-id="dd17b-456">For non-ICM applications, this property determines if ICM is enabled.</span></span> <span data-ttu-id="dd17b-457">Для ICM приложений Система проверяет это свойство, чтобы определить, как обрабатывалась поддержка ICM.</span><span class="sxs-lookup"><span data-stu-id="dd17b-457">For ICM applications, the system examines this property to determine how to handle ICM support.</span></span> <span data-ttu-id="dd17b-458">Это свойство может быть предопределенным значением или заданным драйвером значением, превышающим или равным 256.</span><span class="sxs-lookup"><span data-stu-id="dd17b-458">This property can be a predefined value or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="dd17b-459">Значение определяет, какая система обрабатывает сопоставление цветов изображения.</span><span class="sxs-lookup"><span data-stu-id="dd17b-459">The value determines which system handles image color matching.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dd17b-460">**Отключено** (1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-460">**Disabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows"></span><span id="windows"></span><span id="WINDOWS"></span>

<span data-ttu-id="dd17b-461">**Windows** (2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-461">**Windows** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Driver"></span><span id="device_driver"></span><span id="DEVICE_DRIVER"></span>

<span data-ttu-id="dd17b-462">**Драйвер устройства** (3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-462">**Device Driver** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination_Device"></span><span id="destination_device"></span><span id="DESTINATION_DEVICE"></span>

<span data-ttu-id="dd17b-463">**Целевое устройство** (4)</span><span class="sxs-lookup"><span data-stu-id="dd17b-463">**Destination Device** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-464">**инффиленаме**</span><span class="sxs-lookup"><span data-stu-id="dd17b-464">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-465">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-466">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-467">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ класс управления Win32Registry системы CurrentControlSet \\ \\ \\ \\ \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="dd17b-467">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-468">Путь к INF-файлу видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="dd17b-468">Path to the video adapter's .inf file.</span></span>

<span data-ttu-id="dd17b-469">Пример: "C: \\ \\ драйверы Windows System32 \\ "</span><span class="sxs-lookup"><span data-stu-id="dd17b-469">Example: "C:\\Windows\\SYSTEM32\\DRIVERS"</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-470">**инфсектион**</span><span class="sxs-lookup"><span data-stu-id="dd17b-470">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-471">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-473">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ класс управления Win32Registry системы CurrentControlSet \\ \\ \\ \\ \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="dd17b-473">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-474">INF-файла, в котором находятся сведения о видеоролике Windows.</span><span class="sxs-lookup"><span data-stu-id="dd17b-474">Section of the .inf file where the Windows video information resides.</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-475">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dd17b-475">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-476">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dd17b-476">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-477">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-478">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-479">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="dd17b-479">Date and time the object was installed.</span></span> <span data-ttu-id="dd17b-480">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="dd17b-480">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dd17b-481">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-482">**инсталледдисплайдриверс**</span><span class="sxs-lookup"><span data-stu-id="dd17b-482">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-483">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-484">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-485">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| класс Win32Registry System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-485">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-486">Имя установленного драйвера устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="dd17b-486">Name of the installed display device driver.</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-487">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="dd17b-487">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-488">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-489">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-490">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="dd17b-490">Last error code reported by the logical device.</span></span>

<span data-ttu-id="dd17b-491">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-492">**максмеморисуппортед**</span><span class="sxs-lookup"><span data-stu-id="dd17b-492">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-493">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-494">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-495">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="dd17b-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-496">Максимальный объем поддерживаемой памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="dd17b-496">Maximum amount of memory supported in bytes.</span></span>

<span data-ttu-id="dd17b-497">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-497">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-498">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="dd17b-498">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-499">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-499">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-500">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-501">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-501">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-502">Максимальное число напрямую предоставляемых сущностей, которые поддерживаются этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="dd17b-502">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="dd17b-503">Если число неизвестно, следует использовать значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="dd17b-503">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="dd17b-504">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-504">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-505">**максрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="dd17b-505">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-506">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-507">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-508">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Video \| 003,5 "), [**единицы измерения**](../wmisdk/standard-qualifiers.md) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-508">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-509">Максимальная частота обновления видеоконтроллера в герцах.</span><span class="sxs-lookup"><span data-stu-id="dd17b-509">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="dd17b-510">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-510">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-511">**минрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="dd17b-511">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-512">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-512">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-513">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-514">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Video \| 003,4 "), [**единицы измерения**](../wmisdk/standard-qualifiers.md) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-514">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-515">Минимальная частота обновления видеоконтроллера в герцах.</span><span class="sxs-lookup"><span data-stu-id="dd17b-515">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="dd17b-516">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-516">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-517">**Монохромный**</span><span class="sxs-lookup"><span data-stu-id="dd17b-517">**Monochrome**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-518">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dd17b-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-519">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-520">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dd17b-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-521">**Значение true** показывает, что для вывода изображений используется серый масштаб.</span><span class="sxs-lookup"><span data-stu-id="dd17b-521">If **TRUE**, gray scale is used to display images.</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-522">**Name**</span><span class="sxs-lookup"><span data-stu-id="dd17b-522">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-523">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-524">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-525">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="dd17b-525">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-526">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="dd17b-526">Label by which the object is known.</span></span> <span data-ttu-id="dd17b-527">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="dd17b-527">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="dd17b-528">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-528">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-529">**нумберофколорпланес**</span><span class="sxs-lookup"><span data-stu-id="dd17b-529">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-530">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd17b-530">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-531">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-532">Текущее число цветовых плоскостей.</span><span class="sxs-lookup"><span data-stu-id="dd17b-532">Current number of color planes.</span></span> <span data-ttu-id="dd17b-533">Если это значение неприменимо для текущей конфигурации видео, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="dd17b-533">If this value is not applicable for the current video configuration, enter 0 (zero).</span></span>

<span data-ttu-id="dd17b-534">Это свойство наследуется от [**CIM \_ пквидеоконтроллер**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-534">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-535">**нумберофвидеопажес**</span><span class="sxs-lookup"><span data-stu-id="dd17b-535">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-536">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-536">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-537">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-538">Количество поддерживаемых видео страниц с учетом текущих разрешений и доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="dd17b-538">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="dd17b-539">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-539">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-540">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="dd17b-540">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-541">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-542">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-543">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dd17b-543">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-544">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dd17b-544">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="dd17b-545">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="dd17b-545">Example: "\*PNP030b"</span></span>

<span data-ttu-id="dd17b-546">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-546">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-547">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="dd17b-547">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-548">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dd17b-548">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-549">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-550">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="dd17b-550">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="dd17b-551">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-551">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd17b-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dd17b-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="dd17b-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dd17b-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dd17b-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-556">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="dd17b-556">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="dd17b-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="dd17b-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-558">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="dd17b-558">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="dd17b-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="dd17b-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-560">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="dd17b-560">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="dd17b-561">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="dd17b-561">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="dd17b-562">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-562">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="dd17b-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="dd17b-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-564">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="dd17b-564">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="dd17b-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="dd17b-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-566">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="dd17b-566">Timed Power-On Supported</span></span>

<span data-ttu-id="dd17b-567">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="dd17b-567">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-568">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="dd17b-568">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-569">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dd17b-569">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-570">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-570">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-571">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="dd17b-571">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="dd17b-572">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="dd17b-572">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="dd17b-573">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-574">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="dd17b-574">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-575">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd17b-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-576">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-577">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-577">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-578">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="dd17b-578">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="dd17b-579">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-579">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd17b-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd17b-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="dd17b-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="dd17b-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="dd17b-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="dd17b-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="dd17b-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="dd17b-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="dd17b-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dd17b-586">ATA или ATAPI</span><span class="sxs-lookup"><span data-stu-id="dd17b-586">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="dd17b-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="dd17b-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="dd17b-588"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="dd17b-588"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="dd17b-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="dd17b-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="dd17b-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="dd17b-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="dd17b-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="dd17b-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="dd17b-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="dd17b-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="dd17b-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="dd17b-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="dd17b-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="dd17b-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="dd17b-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="dd17b-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="dd17b-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="dd17b-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="dd17b-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="dd17b-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="dd17b-598"><span id="ESCON"></span><span id="escon"></span>**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="dd17b-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="dd17b-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="dd17b-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="dd17b-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="dd17b-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="dd17b-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="dd17b-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="dd17b-602"><span id="HIPPI"></span><span id="hippi"></span>**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="dd17b-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="dd17b-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="dd17b-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="dd17b-604"><span id="VME"></span><span id="vme"></span>**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="dd17b-604"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="dd17b-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="dd17b-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="dd17b-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="dd17b-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="dd17b-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="dd17b-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="dd17b-608"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="dd17b-608"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="dd17b-609"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="dd17b-609"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="dd17b-610"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="dd17b-610"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="dd17b-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="dd17b-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="dd17b-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="dd17b-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="dd17b-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="dd17b-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="dd17b-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="dd17b-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="dd17b-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="dd17b-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="dd17b-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="dd17b-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="dd17b-617"><span id="IDE"></span><span id="ide"></span>**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="dd17b-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="dd17b-618"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="dd17b-618"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="dd17b-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="dd17b-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="dd17b-620"><span id="DSSI"></span><span id="dssi"></span>**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="dd17b-620"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="dd17b-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="dd17b-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="dd17b-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="dd17b-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="dd17b-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="dd17b-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="dd17b-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="dd17b-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="dd17b-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="dd17b-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="dd17b-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="dd17b-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="dd17b-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="dd17b-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-628">**ресерведсистемпалеттинтриес**</span><span class="sxs-lookup"><span data-stu-id="dd17b-628">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-629">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-629">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-630">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-631">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="dd17b-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-632">Число зарезервированных записей в системной палитре.</span><span class="sxs-lookup"><span data-stu-id="dd17b-632">Number of reserved entries in the system palette.</span></span> <span data-ttu-id="dd17b-633">Операционная система может зарезервировать записи для поддержки стандартных цветов для полос задач и других отображаемых элементов рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="dd17b-633">The operating system may reserve entries to support standard colors for task bars and other desktop display items.</span></span> <span data-ttu-id="dd17b-634">Этот индекс действителен только в том случае, если драйвер устройства задает бит **\_ палитры RC** в индексе растеркапс и доступен только в том случае, если драйвер совместим с 16-разрядной системой Windows.</span><span class="sxs-lookup"><span data-stu-id="dd17b-634">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="dd17b-635">Если в системе не используется палитра, **ресерведсистемпалеттинтриес** не устанавливается.</span><span class="sxs-lookup"><span data-stu-id="dd17b-635">If the system is not using a palette, **ReservedSystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="dd17b-636">Пример: 20</span><span class="sxs-lookup"><span data-stu-id="dd17b-636">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-637">**спеЦификатионверсион**</span><span class="sxs-lookup"><span data-stu-id="dd17b-637">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-638">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-638">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-639">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-639">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-640">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Printing spool Structures \| \| дмспекверсион")</span><span class="sxs-lookup"><span data-stu-id="dd17b-640">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmSpecVersion")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-641">Номер версии спецификации данных инициализации (на которой основана структура).</span><span class="sxs-lookup"><span data-stu-id="dd17b-641">Version number of the initialization data specification (upon which the structure is based).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-642">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="dd17b-642">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-643">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-644">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-644">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-645">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="dd17b-645">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-646">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="dd17b-646">Current status of the object.</span></span> <span data-ttu-id="dd17b-647">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="dd17b-647">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="dd17b-648">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="dd17b-648">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="dd17b-649">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="dd17b-649">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dd17b-650">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="dd17b-650">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dd17b-651">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="dd17b-651">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dd17b-652">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-652">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dd17b-653">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="dd17b-653">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dd17b-654">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="dd17b-654">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dd17b-655">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="dd17b-655">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dd17b-656">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="dd17b-656">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd17b-657">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="dd17b-657">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dd17b-658">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="dd17b-658">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dd17b-659">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="dd17b-659">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dd17b-660">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="dd17b-660">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dd17b-661">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="dd17b-661">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dd17b-662">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="dd17b-662">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dd17b-663">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="dd17b-663">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dd17b-664">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="dd17b-664">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dd17b-665">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="dd17b-665">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-666">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dd17b-666">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-667">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd17b-667">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-668">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-668">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-669">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-669">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-670">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dd17b-670">State of the logical device.</span></span> <span data-ttu-id="dd17b-671">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="dd17b-671">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="dd17b-672">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-672">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd17b-673">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-673">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd17b-674">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-674">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dd17b-675">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-675">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dd17b-676">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="dd17b-676">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dd17b-677">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="dd17b-677">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-678">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="dd17b-678">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-679">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-679">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-680">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-681">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dd17b-681">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-682">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="dd17b-682">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="dd17b-683">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-683">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-684">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dd17b-684">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-685">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-685">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-686">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-687">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dd17b-687">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-688">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="dd17b-688">Name of the scoping system.</span></span>

<span data-ttu-id="dd17b-689">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dd17b-689">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-690">**системпалеттинтриес**</span><span class="sxs-lookup"><span data-stu-id="dd17b-690">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-691">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd17b-691">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-692">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-692">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-693">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="dd17b-693">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-694">Текущее число элементов цветового индекса в системной палитре.</span><span class="sxs-lookup"><span data-stu-id="dd17b-694">Current number of color index entries in the system palette.</span></span> <span data-ttu-id="dd17b-695">Этот индекс действителен только в том случае, если драйвер устройства задает бит **\_ палитры RC** в индексе растеркапс и доступен только в том случае, если драйвер совместим с 16-разрядной системой Windows.</span><span class="sxs-lookup"><span data-stu-id="dd17b-695">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="dd17b-696">Если в системе не используется палитра, **системпалеттинтриес** не устанавливается.</span><span class="sxs-lookup"><span data-stu-id="dd17b-696">If the system is not using a palette, **SystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="dd17b-697">Пример: 20</span><span class="sxs-lookup"><span data-stu-id="dd17b-697">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-698">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="dd17b-698">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-699">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dd17b-699">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-700">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-700">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-701">Дата и время последнего сброса этого контроллера.</span><span class="sxs-lookup"><span data-stu-id="dd17b-701">Date and time this controller was last reset.</span></span> <span data-ttu-id="dd17b-702">Это может означать, что контроллер был отключен или инициализирован повторно.</span><span class="sxs-lookup"><span data-stu-id="dd17b-702">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="dd17b-703">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-703">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-704">**видеоарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="dd17b-704">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-705">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd17b-705">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-706">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-706">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-707">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Video \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-707">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-708">Тип архитектуры видео.</span><span class="sxs-lookup"><span data-stu-id="dd17b-708">Type of video architecture.</span></span>

<span data-ttu-id="dd17b-709">Это свойство наследуется от [**CIM \_ пквидеоконтроллер**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-709">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd17b-710">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-710">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd17b-711">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-711">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="dd17b-712">**КГА** (3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-712">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="dd17b-713">**Ега** (4)</span><span class="sxs-lookup"><span data-stu-id="dd17b-713">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="dd17b-714">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="dd17b-714">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="dd17b-715">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="dd17b-715">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="dd17b-716">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="dd17b-716">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="dd17b-717">**ХГК** (8)</span><span class="sxs-lookup"><span data-stu-id="dd17b-717">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="dd17b-718">**Мкга** (9)</span><span class="sxs-lookup"><span data-stu-id="dd17b-718">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="dd17b-719">**8514A** (10)</span><span class="sxs-lookup"><span data-stu-id="dd17b-719">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="dd17b-720">**Разрешение XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="dd17b-720">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="dd17b-721">**Буфер линейного фрейма** (12)</span><span class="sxs-lookup"><span data-stu-id="dd17b-721">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="dd17b-722">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="dd17b-722">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-723">**видеомеморитипе**</span><span class="sxs-lookup"><span data-stu-id="dd17b-723">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-724">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd17b-724">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-725">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-726">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Video \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-726">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-727">Тип видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="dd17b-727">Type of video memory.</span></span>

<span data-ttu-id="dd17b-728">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-728">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd17b-729">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dd17b-729">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd17b-730">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dd17b-730">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="dd17b-731">**Видеопамять** (3)</span><span class="sxs-lookup"><span data-stu-id="dd17b-731">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="dd17b-732">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="dd17b-732">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="dd17b-733">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="dd17b-733">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="dd17b-734">**Врам** (6)</span><span class="sxs-lookup"><span data-stu-id="dd17b-734">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="dd17b-735">**ОЗУ Эдо** (7)</span><span class="sxs-lookup"><span data-stu-id="dd17b-735">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="dd17b-736">**Пакетная синхронная DRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="dd17b-736">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="dd17b-737">**Конвейерный пакет SRAM** (9)</span><span class="sxs-lookup"><span data-stu-id="dd17b-737">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="dd17b-738">**Кдрам** (10)</span><span class="sxs-lookup"><span data-stu-id="dd17b-738">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="dd17b-739">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="dd17b-739">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="dd17b-740">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="dd17b-740">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="dd17b-741">**Сграм** (13)</span><span class="sxs-lookup"><span data-stu-id="dd17b-741">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd17b-742">**видеомоде**</span><span class="sxs-lookup"><span data-stu-id="dd17b-742">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-743">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd17b-743">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-744">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-744">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-745">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Video \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="dd17b-745">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-746">Текущий видеорежим.</span><span class="sxs-lookup"><span data-stu-id="dd17b-746">Current video mode.</span></span>

<span data-ttu-id="dd17b-747">Это свойство наследуется от [**CIM \_ пквидеоконтроллер**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-747">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-748">**видеомодедескриптион**</span><span class="sxs-lookup"><span data-stu-id="dd17b-748">**VideoModeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-749">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-750">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-750">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-751">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="dd17b-751">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-752">Текущие параметры разрешения, цвета и режима сканирования видеоконтроллера.</span><span class="sxs-lookup"><span data-stu-id="dd17b-752">Current resolution, color, and scan mode settings of the video controller.</span></span>

<span data-ttu-id="dd17b-753">Пример: "1024 x 768 x 256 Colors"</span><span class="sxs-lookup"><span data-stu-id="dd17b-753">Example: "1024 x 768 x 256 colors"</span></span>

</dd> <dt>

<span data-ttu-id="dd17b-754">**видеопроцессор**</span><span class="sxs-lookup"><span data-stu-id="dd17b-754">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd17b-755">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd17b-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd17b-756">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd17b-756">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd17b-757">Произвольная строка, описывающая обработчик видео.</span><span class="sxs-lookup"><span data-stu-id="dd17b-757">Free-form string describing the video processor.</span></span>

<span data-ttu-id="dd17b-758">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-758">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd17b-759">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd17b-759">Remarks</span></span>

<span data-ttu-id="dd17b-760">Класс **Win32 \_ Видеоконтроллер** является производным от [**CIM \_ пквидеоконтроллер**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="dd17b-760">The **Win32\_VideoController** class is derived from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<span data-ttu-id="dd17b-761">Дополнительные сведения об использовании этого класса, например получение сведений с нескольких мониторов, см. [в статье Использование PowerShell для обнаружения сведений о нескольких мониторах](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx).</span><span class="sxs-lookup"><span data-stu-id="dd17b-761">For more information about using this class, such as retrieving information from multiple monitors, see [Use PowerShell to Discover Multi-Monitor Information](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx).</span></span>

## <a name="examples"></a><span data-ttu-id="dd17b-762">Примеры</span><span class="sxs-lookup"><span data-stu-id="dd17b-762">Examples</span></span>

<span data-ttu-id="dd17b-763">В [списке свойства видеоконтроллера](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) в формате VBScript перечислены свойства контроллера видео.</span><span class="sxs-lookup"><span data-stu-id="dd17b-763">The [List Video Controller Properties](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) VBScript sample lists the video controller properties.</span></span>

<span data-ttu-id="dd17b-764">В следующем примере PowerShell перечислены свойства контроллера видео.</span><span class="sxs-lookup"><span data-stu-id="dd17b-764">The following PowerShell example lists the video controller properties.</span></span>


```VB
$strComputer = "." 
 
$colItems = get-wmiobject -class "Win32_VideoController" -namespace "root\CIMV2" ` 
-computername $strComputer 
 
foreach ($objItem in $colItems) { 
      write-host "Accelerator Capabilities: " $objItem.AcceleratorCapabilities 
      write-host "Adapter Compatibility: " $objItem.AdapterCompatibility 
      write-host "Adapter DAC Type: " $objItem.AdapterDACType 
      write-host "Adapter RAM: " $objItem.AdapterRAM 
      write-host "Availability: " $objItem.Availability 
      write-host "Capability Descriptions: " $objItem.CapabilityDescriptions 
      write-host "Caption: " $objItem.Caption 
      write-host "Color Table Entries: " $objItem.ColorTableEntries 
      write-host "Configuration Manager Error Code: " $objItem.ConfigManagerErrorCode 
      write-host "Configuration Manager User Configuration: " $objItem.ConfigManagerUserConfig 
      write-host "Creation Class Name: " $objItem.CreationClassName 
      write-host "Current Bits Per Pixel: " $objItem.CurrentBitsPerPixel 
      write-host "Current Horizontal Resolution: " $objItem.CurrentHorizontalResolution 
      write-host "Current Number Of Colors: " $objItem.CurrentNumberOfColors 
      write-host "Current Number Of Columns: " $objItem.CurrentNumberOfColumns 
      write-host "Current Number Of Rows: " $objItem.CurrentNumberOfRows 
      write-host "Current Refresh Rate: " $objItem.CurrentRefreshRate 
      write-host "Current Scan Mode: " $objItem.CurrentScanMode 
      write-host "Current Vertical Resolution: " $objItem.CurrentVerticalResolution 
      write-host "Description: " $objItem.Description 
      write-host "Device ID: " $objItem.DeviceID 
      write-host "Device Specific Pens: " $objItem.DeviceSpecificPens 
      write-host "Dither Type: " $objItem.DitherType 
      write-host "Driver Date: " $objItem.DriverDate 
      write-host "Driver Version: " $objItem.DriverVersion 
      write-host "Error Cleared: " $objItem.ErrorCleared 
      write-host "Error Description: " $objItem.ErrorDescription 
      write-host "ICM Intent: " $objItem.ICMIntent 
      write-host "ICM Method: " $objItem.ICMMethod 
      write-host "Inf File Name: " $objItem.InfFilename 
      write-host "Inf Section: " $objItem.InfSection 
      write-host "Installation Date: " $objItem.InstallDate 
      write-host "Installed Display Drivers: " $objItem.InstalledDisplayDrivers 
      write-host "Last Error Code: " $objItem.LastErrorCode 
      write-host "Maximum Memory Supported: " $objItem.MaxMemorySupported 
      write-host "Maximum Number Controlled: " $objItem.MaxNumberControlled 
      write-host "Maximum Refresh Rate: " $objItem.MaxRefreshRate 
      write-host "Minimum Refresh Rate: " $objItem.MinRefreshRate 
      write-host "Monochrome: " $objItem.Monochrome 
      write-host "Name: " $objItem.Name 
      write-host "Number Of Color Planes: " $objItem.NumberOfColorPlanes 
      write-host "Number Of Video Pages: " $objItem.NumberOfVideoPages 
      write-host "PNP Device ID: " $objItem.PNPDeviceID 
      write-host "Power Management Capabilities: " $objItem.PowerManagementCapabilities 
      write-host "Power Management Supported: " $objItem.PowerManagementSupported 
      write-host "Protocol Supported: " $objItem.ProtocolSupported 
      write-host "Reserved System Palette Entries: " $objItem.ReservedSystemPaletteEntries 
      write-host "Specification Version: " $objItem.SpecificationVersion 
      write-host "Status: " $objItem.Status 
      write-host "Status Information: " $objItem.StatusInfo 
      write-host "System Creation Class Name: " $objItem.SystemCreationClassName 
      write-host "System Name: " $objItem.SystemName 
      write-host "System Palette Entries: " $objItem.SystemPaletteEntries 
      write-host "Time Of Last Reset: " $objItem.TimeOfLastReset 
      write-host "Video Architecture: " $objItem.VideoArchitecture 
      write-host "Video Memory Type: " $objItem.VideoMemoryType 
      write-host "Video Mode: " $objItem.VideoMode 
      write-host "Video Mode Description: " $objItem.VideoModeDescription 
      write-host "Video Processor: " $objItem.VideoProcessor 
      write-host 
} 
```



## <a name="requirements"></a><span data-ttu-id="dd17b-765">Требования</span><span class="sxs-lookup"><span data-stu-id="dd17b-765">Requirements</span></span>



| <span data-ttu-id="dd17b-766">Требование</span><span class="sxs-lookup"><span data-stu-id="dd17b-766">Requirement</span></span> | <span data-ttu-id="dd17b-767">Значение</span><span class="sxs-lookup"><span data-stu-id="dd17b-767">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd17b-768">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd17b-768">Minimum supported client</span></span><br/> | <span data-ttu-id="dd17b-769">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd17b-769">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd17b-770">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd17b-770">Minimum supported server</span></span><br/> | <span data-ttu-id="dd17b-771">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd17b-771">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd17b-772">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dd17b-772">Namespace</span></span><br/>                | <span data-ttu-id="dd17b-773">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dd17b-773">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd17b-774">MOF</span><span class="sxs-lookup"><span data-stu-id="dd17b-774">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd17b-775"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd17b-775"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd17b-776">DLL</span><span class="sxs-lookup"><span data-stu-id="dd17b-776">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd17b-777"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd17b-777"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd17b-778">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd17b-778">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd17b-779">**\_ПКВИДЕОКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="dd17b-779">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dt>

[<span data-ttu-id="dd17b-780">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="dd17b-780">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
