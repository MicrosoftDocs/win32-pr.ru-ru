---
description: '\_Класс WMI дисплайконтроллерконфигуратион для Win32 представляет сведения о конфигурации видеоадаптера компьютерной системы под Windows.'
ms.assetid: 36ebd840-5e8c-411a-828d-38972fe956e2
ms.tgt_platform: multiple
title: Класс Win32_DisplayControllerConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DisplayControllerConfiguration
- Win32_DisplayControllerConfiguration.Caption
- Win32_DisplayControllerConfiguration.Description
- Win32_DisplayControllerConfiguration.SettingID
- Win32_DisplayControllerConfiguration.BitsPerPixel
- Win32_DisplayControllerConfiguration.ColorPlanes
- Win32_DisplayControllerConfiguration.DeviceEntriesInAColorTable
- Win32_DisplayControllerConfiguration.DeviceSpecificPens
- Win32_DisplayControllerConfiguration.HorizontalResolution
- Win32_DisplayControllerConfiguration.Name
- Win32_DisplayControllerConfiguration.RefreshRate
- Win32_DisplayControllerConfiguration.ReservedSystemPaletteEntries
- Win32_DisplayControllerConfiguration.SystemPaletteEntries
- Win32_DisplayControllerConfiguration.VerticalResolution
- Win32_DisplayControllerConfiguration.VideoMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e64f99cb4d4715d9b7a0eb88bd2e7629feed853
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142280"
---
# <a name="win32_displaycontrollerconfiguration-class"></a><span data-ttu-id="e5fe0-103">\_Класс Win32 дисплайконтроллерконфигуратион</span><span class="sxs-lookup"><span data-stu-id="e5fe0-103">Win32\_DisplayControllerConfiguration class</span></span>

<span data-ttu-id="e5fe0-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ дисплайконтроллерконфигуратион для Win32** представляет сведения о конфигурации видеоадаптера компьютерной системы под Windows.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-104">The **Win32\_DisplayControllerConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the video adapter configuration information of a computer system running Windows.</span></span>

<span data-ttu-id="e5fe0-105">Этот класс устарел.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-105">This class is obsolete.</span></span> <span data-ttu-id="e5fe0-106">Вместо этого класса следует использовать свойства в классах [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ десктопмонитор**](win32-desktopmonitor.md)и [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md) .</span><span class="sxs-lookup"><span data-stu-id="e5fe0-106">In place of this class, you should use the properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes.</span></span>

<span data-ttu-id="e5fe0-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e5fe0-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5fe0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5fe0-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C4E5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DisplayControllerConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 BitsPerPixel;
  uint32 ColorPlanes;
  uint32 DeviceEntriesInAColorTable;
  uint32 DeviceSpecificPens;
  uint32 HorizontalResolution;
  string Name;
  sint32 RefreshRate;
  uint32 ReservedSystemPaletteEntries;
  uint32 SystemPaletteEntries;
  uint32 VerticalResolution;
  string VideoMode;
};
```

## <a name="members"></a><span data-ttu-id="e5fe0-110">Члены</span><span class="sxs-lookup"><span data-stu-id="e5fe0-110">Members</span></span>

<span data-ttu-id="e5fe0-111">Класс **Win32 \_ дисплайконтроллерконфигуратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e5fe0-111">The **Win32\_DisplayControllerConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="e5fe0-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5fe0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5fe0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5fe0-113">Properties</span></span>

<span data-ttu-id="e5fe0-114">Класс **Win32 \_ дисплайконтроллерконфигуратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-114">The **Win32\_DisplayControllerConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5fe0-115">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-115">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-116">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-118">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| битспиксел")</span><span class="sxs-lookup"><span data-stu-id="e5fe0-118">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-119">Число битов, используемых для представления цвета в данной конфигурации, или биты в каждом пикселе.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-119">Either the number of bits used to represent the color in this configuration, or the bits in each pixel.</span></span>

<span data-ttu-id="e5fe0-120">Пример: 8</span><span class="sxs-lookup"><span data-stu-id="e5fe0-120">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-124">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e5fe0-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-125">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-125">Short textual description of the current object.</span></span>

<span data-ttu-id="e5fe0-126">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e5fe0-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-127">**колорпланес**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-127">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-128">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-130">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| плоскости")</span><span class="sxs-lookup"><span data-stu-id="e5fe0-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-131">Текущее число цветовых плоскостей, используемых в конфигурации экрана.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-131">Current number of color planes used in the display configuration.</span></span> <span data-ttu-id="e5fe0-132">Цветовая плоскость — это еще один способ представления цветов пикселей.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-132">A color plane is another way to represent pixel colors.</span></span> <span data-ttu-id="e5fe0-133">Вместо того чтобы назначать одному значению RGB каждому пикселю, цветовые плоскости разделяют изображение на каждый из основных компонентов цвета (красный, зеленый, синий) и сохраняют их на собственных плоскостях.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-133">Instead of assigning a single RGB value to each pixel, color planes separate the graphic into each of the primary color components (red, green, blue), and stores them in their own planes.</span></span> <span data-ttu-id="e5fe0-134">Это обеспечивает более высокую глубину цвета в 8-и 16-разрядных видеосистемах.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-134">This allows for greater color depths on 8-bit and 16-bit video systems.</span></span> <span data-ttu-id="e5fe0-135">Представленные графические системы имеют битвидс, достаточный для хранения информации о глубине цвета. Это означает, что требуется только одна цветовая плоскость.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-135">Present graphics systems have the bitwidth large enough to store color depth information, meaning only one color plane is needed.</span></span>

<span data-ttu-id="e5fe0-136">Пример: 1</span><span class="sxs-lookup"><span data-stu-id="e5fe0-136">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-140">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-140">Textual description of the current object.</span></span>

<span data-ttu-id="e5fe0-141">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e5fe0-141">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-142">**девицеентриесинаколортабле**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-142">**DeviceEntriesInAColorTable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-143">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-145">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| нумколорс")</span><span class="sxs-lookup"><span data-stu-id="e5fe0-145">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-146">Количество цветовых индексов в таблице цветов устройства дисплея (если для устройства задана глубина цвета не более 8 бит на пиксель).</span><span class="sxs-lookup"><span data-stu-id="e5fe0-146">Number of color indexes in a color table of a display device (if the device has a color depth of no more than 8 bits per pixel).</span></span> <span data-ttu-id="e5fe0-147">Для устройств с более высокой глубиной цвета возвращается-1.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-147">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="e5fe0-148">Пример: 256</span><span class="sxs-lookup"><span data-stu-id="e5fe0-148">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-149">**девицеспеЦификпенс**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-149">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-152">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| нумпенс")</span><span class="sxs-lookup"><span data-stu-id="e5fe0-152">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-153">Текущее число перьев, зависящих от устройства.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-153">Current number of device-specific pens.</span></span> <span data-ttu-id="e5fe0-154">Значение 0xFFFFFFFF означает, что устройство не поддерживает перья.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-154">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="e5fe0-155">Перья — это логические свойства, которые могут быть назначены контроллером экрана для отображения устройств и используются для рисования линий, границ многоугольников и текста.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-155">Pens are logical properties that can be assigned by the display controller to display devices, and are used to draw lines, borders of polygons, and text.</span></span>

<span data-ttu-id="e5fe0-156">Пример: 3</span><span class="sxs-lookup"><span data-stu-id="e5fe0-156">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-157">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-157">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-158">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-160">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| хорзрес"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей")</span><span class="sxs-lookup"><span data-stu-id="e5fe0-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-161">Текущее число пикселей в горизонтальном направлении (ось x) дисплея.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-161">Current number of pixels in the horizontal direction (x-axis) of the display.</span></span>

<span data-ttu-id="e5fe0-162">Пример: 1024</span><span class="sxs-lookup"><span data-stu-id="e5fe0-162">Example: 1024</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-163">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-166">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="e5fe0-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-167">Имя адаптера, используемого в этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-167">Name of the adapter used in this configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-168">**рефрешрате**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-168">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-169">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-171">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| хорзресврефреш"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("Герц")</span><span class="sxs-lookup"><span data-stu-id="e5fe0-171">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRESVREFRESH"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-172">Частота обновления видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-172">Refresh rate of the video adapter.</span></span> <span data-ttu-id="e5fe0-173">Значение 0 (ноль) или 1 (одно) указывает, что используется ставка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-173">A value of 0 (zero) or 1 (one) indicates a default rate is being used.</span></span> <span data-ttu-id="e5fe0-174">Значение-1 указывает, что используется оптимальная скорость.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-174">A value of -1 indicates that an optimal rate is being used.</span></span>

<span data-ttu-id="e5fe0-175">Пример: 72</span><span class="sxs-lookup"><span data-stu-id="e5fe0-175">Example: 72</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-176">**ресерведсистемпалеттинтриес**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-176">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-177">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-179">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| нумресервед")</span><span class="sxs-lookup"><span data-stu-id="e5fe0-179">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-180">Текущее число записей цветовых индексов, зарезервированных для использования системой.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-180">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="e5fe0-181">Это значение допустимо только для параметров экрана, использующих индексированную палитру.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-181">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="e5fe0-182">Индексированные палитры не используются для глубины цвета, превышающей 8 бит на пиксель.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-182">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="e5fe0-183">Если глубина цвета превышает 8 бит на пиксель, это значение устанавливается равным **null**.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-183">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="e5fe0-184">Пример: 20</span><span class="sxs-lookup"><span data-stu-id="e5fe0-184">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-185">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-185">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-188">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e5fe0-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-189">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-189">Identifier by which the current object is known.</span></span>

<span data-ttu-id="e5fe0-190">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e5fe0-190">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-191">**системпалеттинтриес**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-191">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-192">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-194">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста устройства \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| нумресервед")</span><span class="sxs-lookup"><span data-stu-id="e5fe0-194">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-195">Текущее число записей цветовых индексов, зарезервированных для использования системой.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-195">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="e5fe0-196">Это значение допустимо только для параметров экрана, использующих индексированную палитру.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-196">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="e5fe0-197">Индексированные палитры не используются для глубины цвета, превышающей 8 бит на пиксель.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-197">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="e5fe0-198">Если глубина цвета превышает 8 бит на пиксель, это значение устанавливается равным **null**.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-198">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="e5fe0-199">Пример: 20</span><span class="sxs-lookup"><span data-stu-id="e5fe0-199">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-200">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-200">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-201">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-203">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| вертрес"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей")</span><span class="sxs-lookup"><span data-stu-id="e5fe0-203">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-204">Текущее число пикселей в вертикальном направлении (ось y) дисплея.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-204">Current number of pixels in the vertical direction (y-axis) of the display.</span></span>

<span data-ttu-id="e5fe0-205">Пример: 768</span><span class="sxs-lookup"><span data-stu-id="e5fe0-205">Example: 768</span></span>

</dd> <dt>

<span data-ttu-id="e5fe0-206">**видеомоде**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-206">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5fe0-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5fe0-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5fe0-209">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="e5fe0-209">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e5fe0-210">Понятное для пользователя описание текущего разрешения экрана и настройки цвета экрана.</span><span class="sxs-lookup"><span data-stu-id="e5fe0-210">User-readable description of the current screen resolution and color setting of the display.</span></span>

<span data-ttu-id="e5fe0-211">Пример: "1024 768 с 256 Colors"</span><span class="sxs-lookup"><span data-stu-id="e5fe0-211">Example: "1024   768 with 256 colors"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5fe0-212">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5fe0-212">Remarks</span></span>

<span data-ttu-id="e5fe0-213">Класс **Win32 \_ дисплайконтроллерконфигуратион** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e5fe0-213">The **Win32\_DisplayControllerConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5fe0-214">Требования</span><span class="sxs-lookup"><span data-stu-id="e5fe0-214">Requirements</span></span>



| <span data-ttu-id="e5fe0-215">Требование</span><span class="sxs-lookup"><span data-stu-id="e5fe0-215">Requirement</span></span> | <span data-ttu-id="e5fe0-216">Значение</span><span class="sxs-lookup"><span data-stu-id="e5fe0-216">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5fe0-217">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5fe0-217">Minimum supported client</span></span><br/> | <span data-ttu-id="e5fe0-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5fe0-218">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5fe0-219">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5fe0-219">Minimum supported server</span></span><br/> | <span data-ttu-id="e5fe0-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5fe0-220">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5fe0-221">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e5fe0-221">Namespace</span></span><br/>                | <span data-ttu-id="e5fe0-222">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e5fe0-222">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e5fe0-223">MOF</span><span class="sxs-lookup"><span data-stu-id="e5fe0-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5fe0-224"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5fe0-224"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5fe0-225">DLL</span><span class="sxs-lookup"><span data-stu-id="e5fe0-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5fe0-226"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5fe0-226"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5fe0-227">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5fe0-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5fe0-228">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="e5fe0-228">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="e5fe0-229">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="e5fe0-229">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

