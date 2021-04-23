---
description: '\_Класс WMI принтерконфигуратион для Win32 представляет конфигурацию для печатающего устройства. Сюда входят такие возможности, как разрешение, цвет, шрифты и ориентация.'
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Класс Win32_PrinterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990696"
---
# <a name="win32_printerconfiguration-class"></a><span data-ttu-id="6ae25-104">\_Класс Win32 принтерконфигуратион</span><span class="sxs-lookup"><span data-stu-id="6ae25-104">Win32\_PrinterConfiguration class</span></span>

<span data-ttu-id="6ae25-105">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ принтерконфигуратион для Win32** представляет конфигурацию для печатающего устройства.</span><span class="sxs-lookup"><span data-stu-id="6ae25-105">The **Win32\_PrinterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the configuration for a printer device.</span></span> <span data-ttu-id="6ae25-106">Сюда входят такие возможности, как разрешение, цвет, шрифты и ориентация.</span><span class="sxs-lookup"><span data-stu-id="6ae25-106">This includes capabilities such as resolution, color, fonts, and orientation.</span></span>

<span data-ttu-id="6ae25-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6ae25-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6ae25-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6ae25-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae25-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ae25-109">Syntax</span></span>

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a><span data-ttu-id="6ae25-110">Члены</span><span class="sxs-lookup"><span data-stu-id="6ae25-110">Members</span></span>

<span data-ttu-id="6ae25-111">Класс **Win32 \_ принтерконфигуратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6ae25-111">The **Win32\_PrinterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="6ae25-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="6ae25-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ae25-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6ae25-113">Properties</span></span>

<span data-ttu-id="6ae25-114">Класс **Win32 \_ принтерконфигуратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6ae25-114">The **Win32\_PrinterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ae25-115">**битсперпел**</span><span class="sxs-lookup"><span data-stu-id="6ae25-115">**BitsPerPel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-116">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-118">Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6ae25-118">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-119">Число битов, используемых для представления цвета в этой конфигурации (бит на пиксель).</span><span class="sxs-lookup"><span data-stu-id="6ae25-119">Number of bits used to represent the color in this configuration (the bits per pixel).</span></span> <span data-ttu-id="6ae25-120">Это свойство устарело.</span><span class="sxs-lookup"><span data-stu-id="6ae25-120">This property is obsolete.</span></span> <span data-ttu-id="6ae25-121">Вместо этого используйте свойства в классах [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ десктопмонитор**](win32-desktopmonitor.md)или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md) , чтобы определить, как представлен цвет.</span><span class="sxs-lookup"><span data-stu-id="6ae25-121">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes to determine how color is represented.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-122">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6ae25-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6ae25-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-125">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="6ae25-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-126">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="6ae25-126">Short textual description of the current object.</span></span>

<span data-ttu-id="6ae25-127">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="6ae25-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-128">**Разобрать по копиям**</span><span class="sxs-lookup"><span data-stu-id="6ae25-128">**Collate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6ae25-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-131">Если **значение равно true**, то печатаемые страницы должны быть упорядочены по копиям.</span><span class="sxs-lookup"><span data-stu-id="6ae25-131">If **TRUE**, the pages that are printed should be collated.</span></span> <span data-ttu-id="6ae25-132">Чтобы выполнить сортировку, необходимо напечатать весь документ перед печатью следующей копии, а не выводить на печать каждую страницу документа необходимое число раз.</span><span class="sxs-lookup"><span data-stu-id="6ae25-132">To collate is to print out the entire document before printing the next copy, as opposed to printing out each page of the document the required number of times.</span></span>

<span data-ttu-id="6ae25-133">Это свойство игнорируется, если драйвер принтера не поддерживает параметры сортировки.</span><span class="sxs-lookup"><span data-stu-id="6ae25-133">This property is ignored unless the printer driver indicates support for collation.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-134">**Цвет**</span><span class="sxs-lookup"><span data-stu-id="6ae25-134">**Color**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-137">Цвет документа.</span><span class="sxs-lookup"><span data-stu-id="6ae25-137">Color of the document.</span></span> <span data-ttu-id="6ae25-138">Некоторые цветовые принтеры могут печататься с помощью черно-белого цвета вместо сочетания голубого, пурпурного и желтого (КМИ).</span><span class="sxs-lookup"><span data-stu-id="6ae25-138">Some color printers have the capability to print using true black instead of a combination of cyan, magenta, and yellow (CMY).</span></span> <span data-ttu-id="6ae25-139">Обычно это позволяет создавать более темный и яркий текст для документов.</span><span class="sxs-lookup"><span data-stu-id="6ae25-139">This usually creates darker and sharper text for documents.</span></span> <span data-ttu-id="6ae25-140">Этот параметр удобен только для цветных принтеров, поддерживающих истинную черновую печать.</span><span class="sxs-lookup"><span data-stu-id="6ae25-140">This option is only useful for color printers that support true black printing.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="6ae25-141"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="6ae25-141"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-142">Монохромный (истинный черный)</span><span class="sxs-lookup"><span data-stu-id="6ae25-142">Monochrome (true black)</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="6ae25-143"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="6ae25-143"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-144">Цвет</span><span class="sxs-lookup"><span data-stu-id="6ae25-144">Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ae25-145">**Копии**</span><span class="sxs-lookup"><span data-stu-id="6ae25-145">**Copies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-148">Число печатаемых копий.</span><span class="sxs-lookup"><span data-stu-id="6ae25-148">Number of copies to be printed.</span></span> <span data-ttu-id="6ae25-149">Драйвер принтера должен поддерживать печать многостраничных копий.</span><span class="sxs-lookup"><span data-stu-id="6ae25-149">The printer driver must support printing multi-page copies.</span></span>

<span data-ttu-id="6ae25-150">Пример: 2</span><span class="sxs-lookup"><span data-stu-id="6ae25-150">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-151">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6ae25-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6ae25-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-154">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="6ae25-154">Textual description of the current object.</span></span>

<span data-ttu-id="6ae25-155">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="6ae25-155">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-156">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="6ae25-156">**DeviceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6ae25-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-159">Понятное имя принтера.</span><span class="sxs-lookup"><span data-stu-id="6ae25-159">Friendly name of the printer.</span></span> <span data-ttu-id="6ae25-160">Это имя является уникальным для типа принтера и может быть усечено из-за ограничений строки, из которой он является производным.</span><span class="sxs-lookup"><span data-stu-id="6ae25-160">This name is unique to the type of printer and may be truncated because of the limitations of the string from which it is derived.</span></span>

<span data-ttu-id="6ae25-161">Пример: PCL или HP LaserJet</span><span class="sxs-lookup"><span data-stu-id="6ae25-161">Example: "PCL/HP LaserJet"</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-162">**дисплайфлагс**</span><span class="sxs-lookup"><span data-stu-id="6ae25-162">**DisplayFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-163">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-165">Указывает, является ли устройство вывода цветным или монохромным, а также тип сканирования — не с чередованием или с чередованием.</span><span class="sxs-lookup"><span data-stu-id="6ae25-165">Indicates whether the display device is color or monochrome and whether the type of scanning is noninterlaced or interlaced.</span></span> <span data-ttu-id="6ae25-166">Это свойство устарело.</span><span class="sxs-lookup"><span data-stu-id="6ae25-166">This property is obsolete.</span></span> <span data-ttu-id="6ae25-167">Вместо этого используйте свойства дисплея, такие как свойство **дисплайтипе** класса **Win32 \_ десктопмонитор** .</span><span class="sxs-lookup"><span data-stu-id="6ae25-167">Instead, use display properties such as the **DisplayType** property of the **Win32\_DesktopMonitor** class.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-168">**дисплайфрекуенци**</span><span class="sxs-lookup"><span data-stu-id="6ae25-168">**DisplayFrequency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-169">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-171">Отображает частоту обновления по вертикали.</span><span class="sxs-lookup"><span data-stu-id="6ae25-171">Displays the vertical refresh rate.</span></span> <span data-ttu-id="6ae25-172">Частота обновления монитора — это число перерисовок экрана в секунду (частота).</span><span class="sxs-lookup"><span data-stu-id="6ae25-172">The refresh rate for a monitor is the number of times the screen is redrawn per second (frequency).</span></span> <span data-ttu-id="6ae25-173">Это свойство устарело.</span><span class="sxs-lookup"><span data-stu-id="6ae25-173">This property is obsolete.</span></span> <span data-ttu-id="6ae25-174">Вместо этого используйте свойства в классе [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ десктопмонитор**](win32-desktopmonitor.md)или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md) .</span><span class="sxs-lookup"><span data-stu-id="6ae25-174">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-175">**дисертипе**</span><span class="sxs-lookup"><span data-stu-id="6ae25-175">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-176">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-178">Тип сглаживания принтера.</span><span class="sxs-lookup"><span data-stu-id="6ae25-178">Dither type of the printer.</span></span> <span data-ttu-id="6ae25-179">Это свойство может принимать стандартные значения от 1 до 5 или определенные драйвером значения от 6 до 256.</span><span class="sxs-lookup"><span data-stu-id="6ae25-179">This property can assume predefined values of 1 to 5, or driver-defined values from 6 to 256.</span></span> <span data-ttu-id="6ae25-180">Дизеринг в виде графика — это специальный метод сглаживания, который обеспечивает четко определенные границы между черным, белым и серым масштабированием.</span><span class="sxs-lookup"><span data-stu-id="6ae25-180">Line art dithering is a special dithering method that produces well defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="6ae25-181">Он не подходит для изображений, которые включают непрерывное окончание интенсивности и оттенков, например отсканированных фотографий.</span><span class="sxs-lookup"><span data-stu-id="6ae25-181">It is not suitable for images that include continuous graduations in intensity and hue, such as scanned photographs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="6ae25-182"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="6ae25-182"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-183">Без сглаживания</span><span class="sxs-lookup"><span data-stu-id="6ae25-183">No Dithering</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="6ae25-184"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="6ae25-184"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-185">Грубая кисть</span><span class="sxs-lookup"><span data-stu-id="6ae25-185">Coarse Brush</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="6ae25-186"><span id="3"></span>**3-5**</span><span class="sxs-lookup"><span data-stu-id="6ae25-186"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-187">Тонкая кисть</span><span class="sxs-lookup"><span data-stu-id="6ae25-187">Fine Brush</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="6ae25-188"><span id="4"></span>**четырех**</span><span class="sxs-lookup"><span data-stu-id="6ae25-188"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-189">График</span><span class="sxs-lookup"><span data-stu-id="6ae25-189">Line Art</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="6ae25-190"><span id="5"></span>**5.0**</span><span class="sxs-lookup"><span data-stu-id="6ae25-190"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-191">Оттенки серого</span><span class="sxs-lookup"><span data-stu-id="6ae25-191">Grayscale</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ae25-192">**дриверверсион**</span><span class="sxs-lookup"><span data-stu-id="6ae25-192">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-193">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-195">Номер версии драйвера принтера на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="6ae25-195">Version number of the Windows-based printer driver.</span></span> <span data-ttu-id="6ae25-196">Номера версий создаются и обслуживаются производителем драйвера.</span><span class="sxs-lookup"><span data-stu-id="6ae25-196">The version numbers are created and maintained by the driver manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-197">**Дуплекс**</span><span class="sxs-lookup"><span data-stu-id="6ae25-197">**Duplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-198">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6ae25-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-200">Если **значение равно true**, печать выполняется на обеих сторонах.</span><span class="sxs-lookup"><span data-stu-id="6ae25-200">If **TRUE**, printing is done on both sides.</span></span> <span data-ttu-id="6ae25-201">Если **значение равно false**, печать выполняется только на одной стороне носителя.</span><span class="sxs-lookup"><span data-stu-id="6ae25-201">If **FALSE**, printing is done on only one side of the media.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-202">**формнаме**</span><span class="sxs-lookup"><span data-stu-id="6ae25-202">**FormName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6ae25-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-205">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6ae25-205">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-206">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="6ae25-206">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-207">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-209">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (точек на дюйм)</span><span class="sxs-lookup"><span data-stu-id="6ae25-209">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-210">Разрешение печати в точках на дюйм вдоль оси x (ширины) задания печати (аналогично устаревшему свойству **ксресолутион** ).</span><span class="sxs-lookup"><span data-stu-id="6ae25-210">Print resolution in dots per inch along the x-axis (width) of the print job (similar to the obsolete **XResolution** property).</span></span> <span data-ttu-id="6ae25-211">Это значение задается, только если свойство **принткуалити** этого класса является положительным.</span><span class="sxs-lookup"><span data-stu-id="6ae25-211">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-212">**икминтент**</span><span class="sxs-lookup"><span data-stu-id="6ae25-212">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-213">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-213">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-215">Конкретное значение одного из трех возможных методов сопоставления цветов (целей), которые должны использоваться по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ae25-215">Specific value of one of the three possible color matching methods (called intents) that should be used by default.</span></span> <span data-ttu-id="6ae25-216">ICM приложения устанавливают намерения, используя функции ICM.</span><span class="sxs-lookup"><span data-stu-id="6ae25-216">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="6ae25-217">Это свойство может принимать стандартные значения от 1 до 3 или определенные драйвером значения от 4 до 256.</span><span class="sxs-lookup"><span data-stu-id="6ae25-217">This property can assume predefined values of 1 to 3, or driver-defined values from 4 to 256.</span></span> <span data-ttu-id="6ae25-218">Приложения, не использующие ICM, могут использовать это значение для определения того, как принтер обрабатывает задания цветовой печати.</span><span class="sxs-lookup"><span data-stu-id="6ae25-218">Non-ICM applications can use this value to determine how the printer handles color printing jobs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="6ae25-219"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="6ae25-219"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-220">Насыщенность</span><span class="sxs-lookup"><span data-stu-id="6ae25-220">Saturation</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="6ae25-221"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="6ae25-221"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-222">Контраст</span><span class="sxs-lookup"><span data-stu-id="6ae25-222">Contrast</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="6ae25-223"><span id="3"></span>**3-5**</span><span class="sxs-lookup"><span data-stu-id="6ae25-223"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-224">Точный цвет</span><span class="sxs-lookup"><span data-stu-id="6ae25-224">Exact Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ae25-225">**икммесод**</span><span class="sxs-lookup"><span data-stu-id="6ae25-225">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-226">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-228">Как обрабатывается ICM.</span><span class="sxs-lookup"><span data-stu-id="6ae25-228">How ICM is handled.</span></span> <span data-ttu-id="6ae25-229">Для приложения, не поддерживающего ICM, это свойство определяет, включен или отключен ICM.</span><span class="sxs-lookup"><span data-stu-id="6ae25-229">For a non-ICM application, this property determines if ICM is enabled or disabled.</span></span> <span data-ttu-id="6ae25-230">Для ICM приложений Система проверяет это свойство, чтобы определить, какая часть системы компьютера обрабатывает поддержку ICM.</span><span class="sxs-lookup"><span data-stu-id="6ae25-230">For ICM applications, the system examines this property to determine which part of the computer system handles ICM support.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="6ae25-231"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="6ae25-231"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-232">Выключено</span><span class="sxs-lookup"><span data-stu-id="6ae25-232">Disabled</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="6ae25-233"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="6ae25-233"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-234">Windows</span><span class="sxs-lookup"><span data-stu-id="6ae25-234">Windows</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="6ae25-235"><span id="3"></span>**3-5**</span><span class="sxs-lookup"><span data-stu-id="6ae25-235"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-236">Драйвер устройства</span><span class="sxs-lookup"><span data-stu-id="6ae25-236">Device Driver</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="6ae25-237"><span id="4"></span>**четырех**</span><span class="sxs-lookup"><span data-stu-id="6ae25-237"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-238">Устройство</span><span class="sxs-lookup"><span data-stu-id="6ae25-238">Device</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ae25-239">**логпикселс**</span><span class="sxs-lookup"><span data-stu-id="6ae25-239">**LogPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-240">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-242">Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6ae25-242">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-243">Число пикселей на логический дюйм.</span><span class="sxs-lookup"><span data-stu-id="6ae25-243">Number of pixels per logical inch.</span></span> <span data-ttu-id="6ae25-244">Это устаревшее свойство допустимо только для устройств, работающих с пикселями, исключая такие устройства, как принтеры.</span><span class="sxs-lookup"><span data-stu-id="6ae25-244">This obsolete property is valid only with devices that work with pixels, which excludes devices such as printers.</span></span> <span data-ttu-id="6ae25-245">Не существует замещающего значения, которое применяется к принтерам.</span><span class="sxs-lookup"><span data-stu-id="6ae25-245">There is no replacement value that applies to printers.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-246">**Мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="6ae25-246">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-247">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-249">Тип носителя, на котором печатается принтер.</span><span class="sxs-lookup"><span data-stu-id="6ae25-249">Type of media on which the printer prints.</span></span> <span data-ttu-id="6ae25-250">Свойству может быть присвоено предопределенное значение или значение, определенное драйвером, которое больше или равно 256.</span><span class="sxs-lookup"><span data-stu-id="6ae25-250">The property can be set to a predefined value or a driver-defined value greater than or equal to 256.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="6ae25-251"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="6ae25-251"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-252">Standard</span><span class="sxs-lookup"><span data-stu-id="6ae25-252">Standard</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="6ae25-253"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="6ae25-253"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-254">Прозрачность</span><span class="sxs-lookup"><span data-stu-id="6ae25-254">Transparency</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="6ae25-255"><span id="3"></span>**3-5**</span><span class="sxs-lookup"><span data-stu-id="6ae25-255"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-256">Глянцевое</span><span class="sxs-lookup"><span data-stu-id="6ae25-256">Glossy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ae25-257">**Name**</span><span class="sxs-lookup"><span data-stu-id="6ae25-257">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6ae25-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-260">Квалификаторы: [**Key**](../wmisdk/standard-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6ae25-260">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-261">Имя принтера, с которым связана эта конфигурация.</span><span class="sxs-lookup"><span data-stu-id="6ae25-261">Name of the printer with which this configuration is associated.</span></span> <span data-ttu-id="6ae25-262">Это значение соответствует свойству **Name** связанного экземпляра [**\_ принтера Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="6ae25-262">This value matches the **Name** property of the associated [**Win32\_Printer**](win32-printer.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-263">**Ориентация**</span><span class="sxs-lookup"><span data-stu-id="6ae25-263">**Orientation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-264">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-266">Ориентация бумаги для печати.</span><span class="sxs-lookup"><span data-stu-id="6ae25-266">Printing orientation of the paper.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="6ae25-267"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="6ae25-267"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-268">Книжная</span><span class="sxs-lookup"><span data-stu-id="6ae25-268">Portrait</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="6ae25-269"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="6ae25-269"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-270">Альбомная</span><span class="sxs-lookup"><span data-stu-id="6ae25-270">Landscape</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ae25-271">**паперленгс**</span><span class="sxs-lookup"><span data-stu-id="6ae25-271">**PaperLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-272">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-274">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (десятые доли миллиметра)</span><span class="sxs-lookup"><span data-stu-id="6ae25-274">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-275">Длина бумаги.</span><span class="sxs-lookup"><span data-stu-id="6ae25-275">Length of the paper.</span></span> <span data-ttu-id="6ae25-276">Чтобы определить размер бумаги в дюймах, разделите это значение на 254.</span><span class="sxs-lookup"><span data-stu-id="6ae25-276">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="6ae25-277">Пример: 2794</span><span class="sxs-lookup"><span data-stu-id="6ae25-277">Example: 2794</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-278">**паперсизе**</span><span class="sxs-lookup"><span data-stu-id="6ae25-278">**PaperSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6ae25-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-281">Размер бумаги.</span><span class="sxs-lookup"><span data-stu-id="6ae25-281">Size of the paper.</span></span> <span data-ttu-id="6ae25-282">Возможные размеры находятся в свойстве **паперсизессуппортед** соответствующего класса [**\_ принтера Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="6ae25-282">The possible sizes are found in the **PaperSizesSupported** property of the associated [**Win32\_Printer**](win32-printer.md) class.</span></span>

<span data-ttu-id="6ae25-283">Пример: "A4 или Letter".</span><span class="sxs-lookup"><span data-stu-id="6ae25-283">Example: "A4 or Letter".</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-284">**папервидс**</span><span class="sxs-lookup"><span data-stu-id="6ae25-284">**PaperWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-285">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-287">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (десятые доли миллиметра)</span><span class="sxs-lookup"><span data-stu-id="6ae25-287">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-288">Ширина бумаги.</span><span class="sxs-lookup"><span data-stu-id="6ae25-288">Width of the paper.</span></span> <span data-ttu-id="6ae25-289">Чтобы определить размер бумаги в дюймах, разделите это значение на 254.</span><span class="sxs-lookup"><span data-stu-id="6ae25-289">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="6ae25-290">Пример: 2159</span><span class="sxs-lookup"><span data-stu-id="6ae25-290">Example: 2159</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-291">**пелшеигхт**</span><span class="sxs-lookup"><span data-stu-id="6ae25-291">**PelsHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-292">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-294">Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6ae25-294">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-295">Данное свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6ae25-295">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-296">**пелсвидс**</span><span class="sxs-lookup"><span data-stu-id="6ae25-296">**PelsWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-297">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-299">Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6ae25-299">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-300">Данное свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6ae25-300">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-301">**PrintQuality**</span><span class="sxs-lookup"><span data-stu-id="6ae25-301">**PrintQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-302">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-304">Один из четырех уровней качества задания печати.</span><span class="sxs-lookup"><span data-stu-id="6ae25-304">One of four quality levels of the print job.</span></span> <span data-ttu-id="6ae25-305">Если указано положительное значение, качество измеряется в точках на дюйм.</span><span class="sxs-lookup"><span data-stu-id="6ae25-305">If a positive value is specified, the quality is measured in dots per inch.</span></span>

<dt>

<span id="-1"></span>

<span data-ttu-id="6ae25-306"><span id="-1"></span>**-1**</span><span class="sxs-lookup"><span data-stu-id="6ae25-306"><span id="-1"></span>**-1**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-307">Черновик</span><span class="sxs-lookup"><span data-stu-id="6ae25-307">Draft</span></span>

</dd> <dt>

<span id="-2"></span>

<span data-ttu-id="6ae25-308"><span id="-2"></span>**-2**</span><span class="sxs-lookup"><span data-stu-id="6ae25-308"><span id="-2"></span>**-2**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-309">Низкий</span><span class="sxs-lookup"><span data-stu-id="6ae25-309">Low</span></span>

</dd> <dt>

<span id="-3"></span>

<span data-ttu-id="6ae25-310"><span id="-3"></span>**-3**</span><span class="sxs-lookup"><span data-stu-id="6ae25-310"><span id="-3"></span>**-3**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-311">Средний</span><span class="sxs-lookup"><span data-stu-id="6ae25-311">Medium</span></span>

</dd> <dt>

<span id="-4"></span>

<span data-ttu-id="6ae25-312"><span id="-4"></span>**по 4**</span><span class="sxs-lookup"><span data-stu-id="6ae25-312"><span id="-4"></span>**-4**</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-313">Высокий</span><span class="sxs-lookup"><span data-stu-id="6ae25-313">High</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ae25-314">**Масштабирование**</span><span class="sxs-lookup"><span data-stu-id="6ae25-314">**Scale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-315">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-317">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (в процентах)</span><span class="sxs-lookup"><span data-stu-id="6ae25-317">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Percent)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-318">Коэффициент, на который должны масштабироваться печатаемые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="6ae25-318">Factor by which the printed output is to be scaled.</span></span> <span data-ttu-id="6ae25-319">Например, масштаб 75 уменьшает вывод на печать до 3/4 ее первоначальной высоты и ширины.</span><span class="sxs-lookup"><span data-stu-id="6ae25-319">For example, a scale of 75 reduces the print output to 3/4 its original height and width.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-320">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="6ae25-320">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6ae25-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-323">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6ae25-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-324">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="6ae25-324">Identifier by which the current object is known.</span></span>

<span data-ttu-id="6ae25-325">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="6ae25-325">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-326">**спеЦификатионверсион**</span><span class="sxs-lookup"><span data-stu-id="6ae25-326">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-327">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-329">Номер версии данных инициализации для устройства, связанного с принтером на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="6ae25-329">Version number of the initialization data for the device associated with the Windows-based printer.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-330">**ттоптион**</span><span class="sxs-lookup"><span data-stu-id="6ae25-330">**TTOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-331">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-333">Указывает, как должны печататься шрифты TrueType.</span><span class="sxs-lookup"><span data-stu-id="6ae25-333">Indicates how TrueType fonts should be printed.</span></span>

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span data-ttu-id="6ae25-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Точечный рисунок** (1)</span><span class="sxs-lookup"><span data-stu-id="6ae25-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-335">Выводит шрифты TrueType в виде графики.</span><span class="sxs-lookup"><span data-stu-id="6ae25-335">Prints TrueType fonts as graphics.</span></span> <span data-ttu-id="6ae25-336">Это действие по умолчанию для принтеров с матричными точками.</span><span class="sxs-lookup"><span data-stu-id="6ae25-336">This is the default action for dot-matrix printers.</span></span>

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span data-ttu-id="6ae25-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Загрузка** (2)</span><span class="sxs-lookup"><span data-stu-id="6ae25-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Download** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-338">Скачивает шрифты TrueType в виде загружаемых шрифтов.</span><span class="sxs-lookup"><span data-stu-id="6ae25-338">Downloads TrueType fonts as soft fonts.</span></span> <span data-ttu-id="6ae25-339">Это действие по умолчанию для принтеров, использующих язык управления принтерами (PCL).</span><span class="sxs-lookup"><span data-stu-id="6ae25-339">This is the default action for printers that use the Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span data-ttu-id="6ae25-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Замена** (3)</span><span class="sxs-lookup"><span data-stu-id="6ae25-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Substitute** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6ae25-341">Замещает шрифты устройства для шрифтов TrueType.</span><span class="sxs-lookup"><span data-stu-id="6ae25-341">Substitutes device fonts for TrueType fonts.</span></span> <span data-ttu-id="6ae25-342">Это действие по умолчанию для принтеров PostScript.</span><span class="sxs-lookup"><span data-stu-id="6ae25-342">This is the default action for PostScript printers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ae25-343">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="6ae25-343">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-344">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-346">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (точек на дюйм)</span><span class="sxs-lookup"><span data-stu-id="6ae25-346">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-347">Разрешение печати вдоль оси y (высота) задания печати (аналогично устаревшему свойству **иресолутион** ).</span><span class="sxs-lookup"><span data-stu-id="6ae25-347">Print resolution along the y-axis (height) of the print job (similar to the obsolete **YResolution** property).</span></span> <span data-ttu-id="6ae25-348">Это значение задается, только если свойство **принткуалити** этого класса является положительным.</span><span class="sxs-lookup"><span data-stu-id="6ae25-348">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-349">**ксресолутион**</span><span class="sxs-lookup"><span data-stu-id="6ae25-349">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-350">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-350">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-352">Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6ae25-352">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-353">Это свойство устарело.</span><span class="sxs-lookup"><span data-stu-id="6ae25-353">This property is obsolete.</span></span> <span data-ttu-id="6ae25-354">Вместо этого используйте свойство **хоризонталресолутион** .</span><span class="sxs-lookup"><span data-stu-id="6ae25-354">Use the **HorizontalResolution** property instead.</span></span>

</dd> <dt>

<span data-ttu-id="6ae25-355">**иресолутион**</span><span class="sxs-lookup"><span data-stu-id="6ae25-355">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ae25-356">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae25-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6ae25-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ae25-358">Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6ae25-358">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6ae25-359">Это свойство устарело.</span><span class="sxs-lookup"><span data-stu-id="6ae25-359">This property is obsolete.</span></span> <span data-ttu-id="6ae25-360">Вместо этого используйте свойство **вертикалресолутион** .</span><span class="sxs-lookup"><span data-stu-id="6ae25-360">Use the **VerticalResolution** property instead.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ae25-361">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ae25-361">Remarks</span></span>

<span data-ttu-id="6ae25-362">Класс **Win32 \_ принтерконфигуратион** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="6ae25-362">The **Win32\_PrinterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="6ae25-363">**Обзор**</span><span class="sxs-lookup"><span data-stu-id="6ae25-363">**Overview**</span></span>

<span data-ttu-id="6ae25-364">Прежде чем можно будет определить оптимальный способ распространения и использования ресурсов печати, необходимо получить подробные сведения об этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="6ae25-364">Before you can determine how to best distribute and use your printing resources, you must have a detailed knowledge of those resources.</span></span> <span data-ttu-id="6ae25-365">Например, в отделе A может быть только три принтера по сравнению с пятью принтерами в отделе б. Однако если принтеры в подразделении A могут печатать 20 страниц в минуту, а принтеры в отделе б могут печатать только 5 страниц в минуту, у пользователей в подразделении есть больше возможностей для печати.</span><span class="sxs-lookup"><span data-stu-id="6ae25-365">For example, Department A might have only three printers compared with five printers in Department B. However, if the printers in Department A can print 20 pages per minute and the printers in Department B can print only 5 pages per minute, users in Department A actually have more printing capacity.</span></span> <span data-ttu-id="6ae25-366">Не зная подробных сведений об этих принтерах, вы можете по ошибке завершить этот отдел а немного поработать с возможностями печати и, таким же, приобрести дополнительные принтеры, которые в итоге будут неиспользуемыми.</span><span class="sxs-lookup"><span data-stu-id="6ae25-366">Without knowing the detailed capabilities of these printers, you might erroneously conclude that Department A is short on printing capacity and thus purchase additional printers that end up going unused.</span></span>

<span data-ttu-id="6ae25-367">WMI включает два класса: [**« \_ принтер Win32**](win32-printer.md) » и « **Win32 \_ принтерконфигуратион**», которые можно использовать для получения подробных сведений обо всех принтерах, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="6ae25-367">WMI includes two classes, [**Win32\_Printer**](win32-printer.md) and **Win32\_PrinterConfiguration**, which can be used to return detailed information about all the printers installed on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="6ae25-368">Примеры</span><span class="sxs-lookup"><span data-stu-id="6ae25-368">Examples</span></span>

<span data-ttu-id="6ae25-369">В следующем примере кода извлекаются сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="6ae25-369">The following code sample retrieves printer information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a><span data-ttu-id="6ae25-370">Требования</span><span class="sxs-lookup"><span data-stu-id="6ae25-370">Requirements</span></span>



| <span data-ttu-id="6ae25-371">Требование</span><span class="sxs-lookup"><span data-stu-id="6ae25-371">Requirement</span></span> | <span data-ttu-id="6ae25-372">Значение</span><span class="sxs-lookup"><span data-stu-id="6ae25-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae25-373">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ae25-373">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae25-374">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ae25-374">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="6ae25-375">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ae25-375">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae25-376">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ae25-376">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="6ae25-377">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6ae25-377">Namespace</span></span><br/>                | <span data-ttu-id="6ae25-378">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6ae25-378">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="6ae25-379">MOF</span><span class="sxs-lookup"><span data-stu-id="6ae25-379">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ae25-380"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ae25-380"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ae25-381">DLL</span><span class="sxs-lookup"><span data-stu-id="6ae25-381">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ae25-382"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ae25-382"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="6ae25-383">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ae25-383">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae25-384">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="6ae25-384">**CIM\_Setting**</span></span>](./cim-setting.md)
</dt> <dt>

[<span data-ttu-id="6ae25-385">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="6ae25-385">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
