---
description: Класс Win32 \_ видеоконфигуратион неактивен. Он не будет возвращать экземпляры, так как поставщик не имеет резервной копии.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Класс Win32_VideoConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96ad4206cc50953a135b23257526ffb5cdc59b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538549"
---
# <a name="win32_videoconfiguration-class"></a><span data-ttu-id="24075-104">\_Класс Win32 видеоконфигуратион</span><span class="sxs-lookup"><span data-stu-id="24075-104">Win32\_VideoConfiguration class</span></span>

<span data-ttu-id="24075-105">Класс **Win32 \_ видеоконфигуратион** неактивен.</span><span class="sxs-lookup"><span data-stu-id="24075-105">The **Win32\_VideoConfiguration** class is not active.</span></span> <span data-ttu-id="24075-106">Он не будет возвращать экземпляры, так как поставщик не имеет резервной копии.</span><span class="sxs-lookup"><span data-stu-id="24075-106">It will not return any instances as there is no provider backing it.</span></span>

<span data-ttu-id="24075-107">Класс **Win32 \_ видеоконфигуратион** представляет конфигурацию подсистемы видео.</span><span class="sxs-lookup"><span data-stu-id="24075-107">The **Win32\_VideoConfiguration** class represents a configuration of a video subsystem.</span></span> <span data-ttu-id="24075-108">Этот класс является устаревшим в пользу свойств, содержащихся в классах [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ десктопмонитор**](win32-desktopmonitor.md)и [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md) .</span><span class="sxs-lookup"><span data-stu-id="24075-108">This class has been deprecated in favor of the properties contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes</span></span>

<span data-ttu-id="24075-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="24075-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="24075-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24075-110">Syntax</span></span>

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="24075-111">Члены</span><span class="sxs-lookup"><span data-stu-id="24075-111">Members</span></span>

<span data-ttu-id="24075-112">Класс **Win32 \_ видеоконфигуратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="24075-112">The **Win32\_VideoConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="24075-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="24075-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24075-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="24075-114">Properties</span></span>

<span data-ttu-id="24075-115">Класс **Win32 \_ видеоконфигуратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="24075-115">The **Win32\_VideoConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24075-116">**актуалколорресолутион**</span><span class="sxs-lookup"><span data-stu-id="24075-116">**ActualColorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-117">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-119">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| колоррес"), [**единицы**](../wmisdk/standard-qualifiers.md) ("бит на пиксель")</span><span class="sxs-lookup"><span data-stu-id="24075-119">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|COLORRES"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per pixel")</span></span>
</dt> </dl>

<span data-ttu-id="24075-120">Указывает текущую глубину цвета для экрана видео.</span><span class="sxs-lookup"><span data-stu-id="24075-120">Indicates the current color depth of the video display.</span></span>

<span data-ttu-id="24075-121">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-121">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-122">**адаптерчиптипе**</span><span class="sxs-lookup"><span data-stu-id="24075-122">**AdapterChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-125">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ сведения о классе \| чиптипе")</span><span class="sxs-lookup"><span data-stu-id="24075-125">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|ChipType")</span></span>
</dt> </dl>

<span data-ttu-id="24075-126">Содержит имя микросхемы адаптера.</span><span class="sxs-lookup"><span data-stu-id="24075-126">Contains the name of the adapter chip.</span></span>

<span data-ttu-id="24075-127">Пример: S3</span><span class="sxs-lookup"><span data-stu-id="24075-127">Example: s3</span></span>

<span data-ttu-id="24075-128">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-128">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-129">**адаптеркомпатибилити**</span><span class="sxs-lookup"><span data-stu-id="24075-129">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-132">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**ключ**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="24075-132">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="24075-133">Указывает имя производителя адаптера.</span><span class="sxs-lookup"><span data-stu-id="24075-133">Specifies the name of the manufacturer of the adapter.</span></span> <span data-ttu-id="24075-134">Это имя можно использовать для сравнения совместимости этого устройства с потребностями компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="24075-134">This name can be used to compare the compatibility of this device with the needs of the computer system.</span></span>

<span data-ttu-id="24075-135">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-135">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-136">**адаптердактипе**</span><span class="sxs-lookup"><span data-stu-id="24075-136">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-139">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ сведения о классе \| DACType")</span><span class="sxs-lookup"><span data-stu-id="24075-139">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|DACType")</span></span>
</dt> </dl>

<span data-ttu-id="24075-140">Указывает имя микросхемы с цифровым подключением (DAC), используемой в адаптере.</span><span class="sxs-lookup"><span data-stu-id="24075-140">Indicates the name of the digital-to-analog chip (DAC) used in the adapter.</span></span>

<span data-ttu-id="24075-141">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-141">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-142">**адаптердескриптион**</span><span class="sxs-lookup"><span data-stu-id="24075-142">**AdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-145">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="24075-145">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="24075-146">Содержит описание или описательное имя видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="24075-146">Contains a description or descriptive name of the video adapter.</span></span>

<span data-ttu-id="24075-147">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-147">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-148">**адаптеррам**</span><span class="sxs-lookup"><span data-stu-id="24075-148">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-151">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ сведения о классе \| видеомемори"), [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="24075-151">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="24075-152">Указывает объем памяти видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="24075-152">Indicates the memory size of the video adapter.</span></span>

<span data-ttu-id="24075-153">Пример: 16777216</span><span class="sxs-lookup"><span data-stu-id="24075-153">Example: 16777216</span></span>

<span data-ttu-id="24075-154">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-154">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-155">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="24075-155">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-158">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| система описания оборудования Win32Registry \\ \\ \\ \\ \\ \\ дисплайконтроллер \\ \\ 0 \\ \\ идентификатор")</span><span class="sxs-lookup"><span data-stu-id="24075-158">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\DisplayController\\\\0\\\\Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="24075-159">Указывает тип видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="24075-159">Indicates the type of video adapter.</span></span>

<span data-ttu-id="24075-160">Кодировка: буквенно-цифровой</span><span class="sxs-lookup"><span data-stu-id="24075-160">Character Set: Alphanumeric</span></span>

<span data-ttu-id="24075-161">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-161">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-162">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="24075-162">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-163">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-165">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| битспиксел")</span><span class="sxs-lookup"><span data-stu-id="24075-165">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="24075-166">Указывает фактическое число битов на пиксель, представляющих дисплей.</span><span class="sxs-lookup"><span data-stu-id="24075-166">Indicates the actual number of bits per pixel representing the display.</span></span> <span data-ttu-id="24075-167">Оно может масштабироваться до текущего параметра видео (представленного свойством Актуалколорресолутион) пользователя.</span><span class="sxs-lookup"><span data-stu-id="24075-167">This may be scaled to the current video setting (represented by the ActualColorResolution property) of the user.</span></span>

<span data-ttu-id="24075-168">Пример: 8</span><span class="sxs-lookup"><span data-stu-id="24075-168">Example: 8</span></span>

<span data-ttu-id="24075-169">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-169">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-170">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="24075-170">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-173">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="24075-173">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="24075-174">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="24075-174">Short textual description of the current object.</span></span>

<span data-ttu-id="24075-175">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="24075-175">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-176">**колорпланес**</span><span class="sxs-lookup"><span data-stu-id="24075-176">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-177">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-179">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| плоскости")</span><span class="sxs-lookup"><span data-stu-id="24075-179">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="24075-180">Указывает текущее число цветовых плоскостей, используемых в видеомониторе.</span><span class="sxs-lookup"><span data-stu-id="24075-180">Indicates the current number of color planes used in the video display.</span></span> <span data-ttu-id="24075-181">Цветовая панель — это еще один способ представления цветов пикселей. Вместо того чтобы назначать одному значению RGB каждому пикселю, цветовые плоскости разделяют изображение на каждый из основных компонентов цвета (красный зеленый цвет) и сохраняют их на собственных плоскостях.</span><span class="sxs-lookup"><span data-stu-id="24075-181">A color plane is another way to represent pixel colors; instead of assigning a single RGB value to each a pixel, color planes separate the graphic into each of the primary color components (red green blue), and store them in their own planes.</span></span> <span data-ttu-id="24075-182">Это обеспечивает более высокую глубину цвета в 8 и 16 разрядных видеосистемах.</span><span class="sxs-lookup"><span data-stu-id="24075-182">This allows for greater color depths on 8 and 16 bit video systems.</span></span> <span data-ttu-id="24075-183">Представленные графические системы имеют битвидс, достаточный для хранения информации о глубине цвета, что делает обязательным только одну цветовую плоскость.</span><span class="sxs-lookup"><span data-stu-id="24075-183">Present graphics systems have the bitwidth large enough to store color depth information, making only one color plane necessary.</span></span>

<span data-ttu-id="24075-184">Пример: 1</span><span class="sxs-lookup"><span data-stu-id="24075-184">Example: 1</span></span>

<span data-ttu-id="24075-185">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-185">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-186">**колортаблинтриес**</span><span class="sxs-lookup"><span data-stu-id="24075-186">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-187">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-189">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| нумколорс")</span><span class="sxs-lookup"><span data-stu-id="24075-189">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="24075-190">Указывает количество цветовых индексов в таблице цветов для экрана видео.</span><span class="sxs-lookup"><span data-stu-id="24075-190">Indicates the number of color indexes in a color table for a video display.</span></span> <span data-ttu-id="24075-191">Это свойство используется, если цветовая глубина устройства не превышает 8 бит на пиксель.</span><span class="sxs-lookup"><span data-stu-id="24075-191">This property is used if the device has a color depth of no more than 8 bits per pixel.</span></span> <span data-ttu-id="24075-192">Для устройств с более высокой глубиной цвета возвращается-1.</span><span class="sxs-lookup"><span data-stu-id="24075-192">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="24075-193">Пример: 256</span><span class="sxs-lookup"><span data-stu-id="24075-193">Example: 256</span></span>

<span data-ttu-id="24075-194">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-194">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-195">**Описание**</span><span class="sxs-lookup"><span data-stu-id="24075-195">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24075-198">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="24075-198">Textual description of the current object.</span></span>

<span data-ttu-id="24075-199">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="24075-199">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-200">**девицеспеЦификпенс**</span><span class="sxs-lookup"><span data-stu-id="24075-200">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-201">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-203">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| нумпенс")</span><span class="sxs-lookup"><span data-stu-id="24075-203">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="24075-204">Указывает текущее число перьев конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="24075-204">Indicates the current number of device-specific pens.</span></span> <span data-ttu-id="24075-205">Значение 0xFFFFFFFF означает, что устройство не поддерживает перья.</span><span class="sxs-lookup"><span data-stu-id="24075-205">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="24075-206">Перья используются для рисования линий и себордерс объектов многоугольников.</span><span class="sxs-lookup"><span data-stu-id="24075-206">Pens are used to draw lines and theborders of polygonal objects.</span></span>

<span data-ttu-id="24075-207">Пример: 3</span><span class="sxs-lookup"><span data-stu-id="24075-207">Example: 3</span></span>

<span data-ttu-id="24075-208">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-208">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-209">**дривердате**</span><span class="sxs-lookup"><span data-stu-id="24075-209">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-210">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="24075-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="24075-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-212">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ класса \\ \\ адаптердескриптион \| дривердате")</span><span class="sxs-lookup"><span data-stu-id="24075-212">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\AdapterDescription\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="24075-213">Указывает дату и время установки текущего видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="24075-213">Indicates the date and time the current video driver was installed.</span></span>

<span data-ttu-id="24075-214">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-214">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-215">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="24075-215">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-216">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-218">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| хорзрес")</span><span class="sxs-lookup"><span data-stu-id="24075-218">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES")</span></span>
</dt> </dl>

<span data-ttu-id="24075-219">Указывает текущее количество пикселей в горизонтальном направлении (на оси X) дисплея.</span><span class="sxs-lookup"><span data-stu-id="24075-219">Indicates the current number of pixels in the horizontal direction (X axis) of the display.</span></span>

<span data-ttu-id="24075-220">Пример: 1024</span><span class="sxs-lookup"><span data-stu-id="24075-220">Example: 1024</span></span>

<span data-ttu-id="24075-221">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-221">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-222">**инффиленаме**</span><span class="sxs-lookup"><span data-stu-id="24075-222">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-225">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \| инфпас")</span><span class="sxs-lookup"><span data-stu-id="24075-225">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="24075-226">Указывает путь к INF-файлу видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="24075-226">Specifies the path to the .inf file of the video driver.</span></span>

<span data-ttu-id="24075-227">Пример: C: \\ \\ драйверы Windows System32 \\</span><span class="sxs-lookup"><span data-stu-id="24075-227">Example: C:\\Windows\\System32\\Drivers</span></span>

<span data-ttu-id="24075-228">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-228">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-229">**инфсектион**</span><span class="sxs-lookup"><span data-stu-id="24075-229">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-232">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \| инфсектион")</span><span class="sxs-lookup"><span data-stu-id="24075-232">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="24075-233">Указывает раздел INF-файла, в котором находится информация о видео Win32.</span><span class="sxs-lookup"><span data-stu-id="24075-233">Indicates the section of the .inf file where the Win32 video information resides.</span></span>

<span data-ttu-id="24075-234">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-234">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-235">**инсталледдисплайдриверс**</span><span class="sxs-lookup"><span data-stu-id="24075-235">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-236">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-238">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ \\ дефауле \| drv")</span><span class="sxs-lookup"><span data-stu-id="24075-238">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Defaule\|drv")</span></span>
</dt> </dl>

<span data-ttu-id="24075-239">Указывает имя установленного видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="24075-239">Indicates the name of the installed video driver.</span></span>

<span data-ttu-id="24075-240">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-240">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-241">**монитормануфактурер**</span><span class="sxs-lookup"><span data-stu-id="24075-241">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-244">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="24075-244">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="24075-245">Указывает имя изготовителя устройства дисплея.</span><span class="sxs-lookup"><span data-stu-id="24075-245">Indicates the name of the manufacturer of the display device.</span></span>

<span data-ttu-id="24075-246">Пример: NEC</span><span class="sxs-lookup"><span data-stu-id="24075-246">Example: NEC</span></span>

<span data-ttu-id="24075-247">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-247">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-248">**Тип монитора "**</span><span class="sxs-lookup"><span data-stu-id="24075-248">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-251">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| система описания оборудования Win32Registry \\ \\ \\ \\ \\ \\ мониторпериферал \\ \\ 0 \| идентификатор")</span><span class="sxs-lookup"><span data-stu-id="24075-251">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\MonitorPeripheral\\\\0\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="24075-252">Указывает имя модели устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="24075-252">Indicates the model name of the display device.</span></span>

<span data-ttu-id="24075-253">Пример: NEC 5FGp</span><span class="sxs-lookup"><span data-stu-id="24075-253">Example: NEC 5FGp</span></span>

<span data-ttu-id="24075-254">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-254">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-255">**Name**</span><span class="sxs-lookup"><span data-stu-id="24075-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-256">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-258">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**ключ**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="24075-258">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="24075-259">Содержит идентифицирующее имя для класса конфигурации видео.</span><span class="sxs-lookup"><span data-stu-id="24075-259">Contains an identifying name for the video configuration class.</span></span>

<span data-ttu-id="24075-260">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-260">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-261">**пикселсперкслогикалинч**</span><span class="sxs-lookup"><span data-stu-id="24075-261">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-262">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-264">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| логпикселскс")</span><span class="sxs-lookup"><span data-stu-id="24075-264">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSX")</span></span>
</dt> </dl>

<span data-ttu-id="24075-265">Указывает число пикселов на логический дюйм по оси X (горизонтальное направление) дисплея.</span><span class="sxs-lookup"><span data-stu-id="24075-265">Indicates the number of pixels per logical inch along the X axis (horizontal direction) of the display.</span></span>

<span data-ttu-id="24075-266">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-266">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-267">**пикселсперилогикалинч**</span><span class="sxs-lookup"><span data-stu-id="24075-267">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-268">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-270">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| логпикселси")</span><span class="sxs-lookup"><span data-stu-id="24075-270">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSY")</span></span>
</dt> </dl>

<span data-ttu-id="24075-271">Указывает число пикселей на логический дюйм по оси Y (вертикальное направление) дисплея.</span><span class="sxs-lookup"><span data-stu-id="24075-271">Indicates the number of pixels per logical inch along the Y axis (vertical direction) of the display.</span></span>

<span data-ttu-id="24075-272">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-272">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-273">**рефрешрате**</span><span class="sxs-lookup"><span data-stu-id="24075-273">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-274">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-276">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| врефреш")</span><span class="sxs-lookup"><span data-stu-id="24075-276">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VREFRESH")</span></span>
</dt> </dl>

<span data-ttu-id="24075-277">Указывает частоту обновления конфигурации видео.</span><span class="sxs-lookup"><span data-stu-id="24075-277">Indicates the refresh rate of the video configuration.</span></span> <span data-ttu-id="24075-278">Значение 0 или 1 указывает, что используется ставка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24075-278">A value of 0 or 1 indicates a default rate is being used.</span></span>

<span data-ttu-id="24075-279">Пример: 72</span><span class="sxs-lookup"><span data-stu-id="24075-279">Example: 72</span></span>

<span data-ttu-id="24075-280">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-280">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-281">**сканмоде**</span><span class="sxs-lookup"><span data-stu-id="24075-281">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-282">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-284">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| дефаултсеттингс. Чересстрочная развертка")</span><span class="sxs-lookup"><span data-stu-id="24075-284">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Device0\|DefaultSettings.Interlaced")</span></span>
</dt> </dl>

<span data-ttu-id="24075-285">Указывает, является ли устройство вывода чередованием.</span><span class="sxs-lookup"><span data-stu-id="24075-285">Indicates whether the display device is interlaced.</span></span>

<span data-ttu-id="24075-286">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-286">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="24075-287">**Без чередования** ("без чередования")</span><span class="sxs-lookup"><span data-stu-id="24075-287">**Non Interlaced** ("Non Interlaced")</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="24075-288">С **чередованием** (чередование)</span><span class="sxs-lookup"><span data-stu-id="24075-288">**Interlaced** ("Interlaced")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24075-289">**скринхеигхт**</span><span class="sxs-lookup"><span data-stu-id="24075-289">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-290">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-292">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| вертсизе"), [**единицы измерения**](../wmisdk/standard-qualifiers.md) ("миллиметры")</span><span class="sxs-lookup"><span data-stu-id="24075-292">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="24075-293">Задает высоту физического экрана.</span><span class="sxs-lookup"><span data-stu-id="24075-293">Specifies the height of the physical screen.</span></span>

<span data-ttu-id="24075-294">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-294">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-295">**скринвидс**</span><span class="sxs-lookup"><span data-stu-id="24075-295">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-296">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-298">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| хорзсизе"), [**единицы измерения**](../wmisdk/standard-qualifiers.md) ("миллиметры")</span><span class="sxs-lookup"><span data-stu-id="24075-298">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="24075-299">Задает ширину физического экрана.</span><span class="sxs-lookup"><span data-stu-id="24075-299">Specifies the width of the physical screen.</span></span>

<span data-ttu-id="24075-300">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-300">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-301">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="24075-301">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-302">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24075-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24075-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-304">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="24075-304">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="24075-305">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="24075-305">Identifier by which the current object is known.</span></span>

<span data-ttu-id="24075-306">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="24075-306">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-307">**системпалеттинтриес**</span><span class="sxs-lookup"><span data-stu-id="24075-307">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-308">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-310">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| сизепалетте")</span><span class="sxs-lookup"><span data-stu-id="24075-310">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|SIZEPALETTE")</span></span>
</dt> </dl>

<span data-ttu-id="24075-311">Реализовано текущее количество записей цветовых индексов, зарезервированных для использования системой.</span><span class="sxs-lookup"><span data-stu-id="24075-311">Iindicates the current number of color index entries reserved for system use.</span></span> <span data-ttu-id="24075-312">Это значение допустимо только для параметров экрана, использующих индексированную палитру.</span><span class="sxs-lookup"><span data-stu-id="24075-312">This value is only valid for display settings that use an indexed palette .</span></span> <span data-ttu-id="24075-313">Индексированные палитры не используются для глубины цвета, превышающей 8 бит на пиксель.</span><span class="sxs-lookup"><span data-stu-id="24075-313">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="24075-314">Если глубина цвета превышает 8 бит на пиксель, это значение устанавливается равным **null**.</span><span class="sxs-lookup"><span data-stu-id="24075-314">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="24075-315">Пример: 20</span><span class="sxs-lookup"><span data-stu-id="24075-315">Example: 20</span></span>

<span data-ttu-id="24075-316">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-316">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="24075-317">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="24075-317">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24075-318">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24075-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24075-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24075-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24075-320">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| вертрес")</span><span class="sxs-lookup"><span data-stu-id="24075-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES")</span></span>
</dt> </dl>

<span data-ttu-id="24075-321">Указывает текущее количество пикселей в вертикальном направлении (ось Y) дисплея.</span><span class="sxs-lookup"><span data-stu-id="24075-321">Indicates the current number of pixels in the vertical direction (Y axis) of the display.</span></span>

<span data-ttu-id="24075-322">Пример: 768</span><span class="sxs-lookup"><span data-stu-id="24075-322">Example: 768</span></span>

<span data-ttu-id="24075-323">Это свойство не рекомендуется использовать в пользу соответствующих свойств, содержащихся в [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ Десктопмонитор**](win32-desktopmonitor.md) и//или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="24075-323">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24075-324">Требования</span><span class="sxs-lookup"><span data-stu-id="24075-324">Requirements</span></span>



| <span data-ttu-id="24075-325">Требование</span><span class="sxs-lookup"><span data-stu-id="24075-325">Requirement</span></span> | <span data-ttu-id="24075-326">Значение</span><span class="sxs-lookup"><span data-stu-id="24075-326">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24075-327">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24075-327">Minimum supported client</span></span><br/> | <span data-ttu-id="24075-328">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24075-328">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24075-329">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24075-329">Minimum supported server</span></span><br/> | <span data-ttu-id="24075-330">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24075-330">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24075-331">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="24075-331">Namespace</span></span><br/>                | <span data-ttu-id="24075-332">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="24075-332">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="24075-333">MOF</span><span class="sxs-lookup"><span data-stu-id="24075-333">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24075-334"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24075-334"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="24075-335">DLL</span><span class="sxs-lookup"><span data-stu-id="24075-335">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24075-336"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24075-336"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24075-337">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24075-337">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24075-338">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="24075-338">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

 
