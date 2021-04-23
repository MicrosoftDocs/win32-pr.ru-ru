---
description: Представляет контроллер дисплея.
ms.assetid: 14598ae6-58e2-46ca-8653-b57e5833a224
title: Класс CIM_DisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DisplayController
- CIM_DisplayController.Description
- CIM_DisplayController.VideoProcessor
- CIM_DisplayController.VideoMemoryType
- CIM_DisplayController.OtherVideoMemoryType
- CIM_DisplayController.NumberOfVideoPages
- CIM_DisplayController.MaxMemorySupported
- CIM_DisplayController.AcceleratorCapabilities
- CIM_DisplayController.CapabilityDescriptions
- CIM_DisplayController.OtherVideoArchitecture
- CIM_DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59db37a89ce1f57e01a6a9a27fb9c24177221b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682943"
---
# <a name="cim_displaycontroller-class"></a><span data-ttu-id="38848-103">\_Класс CIM дисплайконтроллер</span><span class="sxs-lookup"><span data-stu-id="38848-103">CIM\_DisplayController class</span></span>

<span data-ttu-id="38848-104">Представляет контроллер дисплея.</span><span class="sxs-lookup"><span data-stu-id="38848-104">Represents a display controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="38848-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38848-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_DisplayController : CIM_Controller
{
  string Description;
  string VideoProcessor;
  uint16 VideoMemoryType;
  string OtherVideoMemoryType;
  uint32 NumberOfVideoPages;
  uint32 MaxMemorySupported;
  uint16 AcceleratorCapabilities[];
  string CapabilityDescriptions[];
  string OtherVideoArchitecture;
  uint16 VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="38848-106">Члены</span><span class="sxs-lookup"><span data-stu-id="38848-106">Members</span></span>

<span data-ttu-id="38848-107">Класс **CIM \_ дисплайконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="38848-107">The **CIM\_DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="38848-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="38848-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38848-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="38848-109">Properties</span></span>

<span data-ttu-id="38848-110">Класс **CIM \_ дисплайконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="38848-110">The **CIM\_DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38848-111">**акцелераторкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="38848-111">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38848-112">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="38848-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="38848-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38848-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38848-114">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ дисплайконтроллер**.**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="38848-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="38848-115">Графические и трехмерные возможности контроллера экрана.</span><span class="sxs-lookup"><span data-stu-id="38848-115">The graphics and 3D capabilities of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="38848-116">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="38848-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="38848-117">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="38848-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="38848-118">**Графический ускоритель** (2)</span><span class="sxs-lookup"><span data-stu-id="38848-118">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="38848-119">**трехмерный ускоритель** (3)</span><span class="sxs-lookup"><span data-stu-id="38848-119">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Fast_Write"></span><span id="pci_fast_write"></span><span id="PCI_FAST_WRITE"></span>

<span data-ttu-id="38848-120">**Быстрая запись PCI** (4)</span><span class="sxs-lookup"><span data-stu-id="38848-120">**PCI Fast Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiMonitor_Support"></span><span id="multimonitor_support"></span><span id="MULTIMONITOR_SUPPORT"></span>

<span data-ttu-id="38848-121">**Поддержка многомониторной поддержки** (5)</span><span class="sxs-lookup"><span data-stu-id="38848-121">**MultiMonitor Support** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Mastering"></span><span id="pci_mastering"></span><span id="PCI_MASTERING"></span>

<span data-ttu-id="38848-122">**Главный PCI** (6)</span><span class="sxs-lookup"><span data-stu-id="38848-122">**PCI Mastering** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Second_Monochrome_Adapter_Support"></span><span id="second_monochrome_adapter_support"></span><span id="SECOND_MONOCHROME_ADAPTER_SUPPORT"></span>

<span data-ttu-id="38848-123">**Поддержка второго монохромного адаптера** (7)</span><span class="sxs-lookup"><span data-stu-id="38848-123">**Second Monochrome Adapter Support** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Large_Memory_Address_Support"></span><span id="large_memory_address_support"></span><span id="LARGE_MEMORY_ADDRESS_SUPPORT"></span>

<span data-ttu-id="38848-124">**Поддержка адресов большого объема памяти** (8)</span><span class="sxs-lookup"><span data-stu-id="38848-124">**Large Memory Address Support** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38848-125">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="38848-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38848-126">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="38848-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="38848-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38848-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38848-128">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ дисплайконтроллер**.**Акцелераторкапабилитиес**")</span><span class="sxs-lookup"><span data-stu-id="38848-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="38848-129">Подробное объяснение возможностей ускорителя видео массива **акцелераторкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="38848-129">Detailed explanations for video accelerator features of the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="38848-130">Элементы в этом массиве соответствуют элементам массива в **акцелераторкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="38848-130">The items in this array correspond to the array items in **AcceleratorCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="38848-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="38848-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38848-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38848-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38848-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38848-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38848-134">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,18 ")</span><span class="sxs-lookup"><span data-stu-id="38848-134">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.18")</span></span>
</dt> </dl>

<span data-ttu-id="38848-135">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="38848-135">A text description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="38848-136">**максмеморисуппортед**</span><span class="sxs-lookup"><span data-stu-id="38848-136">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38848-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38848-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38848-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38848-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38848-139">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="38848-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="38848-140">Максимальный поддерживаемый объем памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="38848-140">The maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="38848-141">**нумберофвидеопажес**</span><span class="sxs-lookup"><span data-stu-id="38848-141">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38848-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38848-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38848-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38848-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38848-144">Число поддерживаемых страниц видео с учетом текущих разрешений и доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="38848-144">The number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="38848-145">**осервидеоарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="38848-145">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38848-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38848-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38848-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38848-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38848-148">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ дисплайконтроллер**.**Видеоарчитектуре**")</span><span class="sxs-lookup"><span data-stu-id="38848-148">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoArchitecture**")</span></span>
</dt> </dl>

<span data-ttu-id="38848-149">Описание типа архитектуры видео, если свойство **видеоарчитектуре** содержит значение "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="38848-149">A description of the video architecture type when the **VideoArchitecture** property contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="38848-150">**осервидеомеморитипе**</span><span class="sxs-lookup"><span data-stu-id="38848-150">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38848-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38848-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38848-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38848-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38848-153">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ дисплайконтроллер**.**Видеомеморитипе**")</span><span class="sxs-lookup"><span data-stu-id="38848-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="38848-154">Тип видеопамяти, если свойство **видеомеморитипе** имеет значение "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="38848-154">The video memory type when the **VideoMemoryType** property is "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="38848-155">**видеоарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="38848-155">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38848-156">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38848-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38848-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38848-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38848-158">Архитектура видео контроллеров экрана, используемая для создания видеосигнала.</span><span class="sxs-lookup"><span data-stu-id="38848-158">The display controllers video architecture used to generate the video signal.</span></span> <span data-ttu-id="38848-159">Обычно выделенный видеопроцессор создает видеосигнал в соответствии с указанной архитектурой.</span><span class="sxs-lookup"><span data-stu-id="38848-159">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="38848-160">Архитектура указывает на максимальную возможность разрешения контроллера экрана.</span><span class="sxs-lookup"><span data-stu-id="38848-160">The architecture indicates of the maximum resolution capability of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="38848-161">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="38848-161">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="38848-162">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="38848-162">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="38848-163">**КГА** (2)</span><span class="sxs-lookup"><span data-stu-id="38848-163">**CGA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="38848-164">**Ега** (3)</span><span class="sxs-lookup"><span data-stu-id="38848-164">**EGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="38848-165">**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="38848-165">**VGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="38848-166">**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="38848-166">**SVGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="38848-167">**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="38848-167">**MDA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="38848-168">**ХГК** (7)</span><span class="sxs-lookup"><span data-stu-id="38848-168">**HGC** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="38848-169">**Мкга** (8)</span><span class="sxs-lookup"><span data-stu-id="38848-169">**MCGA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="38848-170">**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="38848-170">**8514A** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="38848-171">**Разрешение XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="38848-171">**XGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="38848-172">**Буфер линейного фрейма** (11)</span><span class="sxs-lookup"><span data-stu-id="38848-172">**Linear Frame Buffer** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="38848-173">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="38848-173">**PC-98** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="38848-174">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="38848-174">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="38848-175">**Поставщик зарезервирован** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="38848-175">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38848-176">**видеомеморитипе**</span><span class="sxs-lookup"><span data-stu-id="38848-176">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38848-177">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38848-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38848-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38848-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38848-179">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 004,6 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ дисплайконтроллер**.**Осервидеомеморитипе**")</span><span class="sxs-lookup"><span data-stu-id="38848-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.6"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**OtherVideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="38848-180">Тип видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="38848-180">The type of video memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="38848-181">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="38848-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="38848-182">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="38848-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="38848-183">**Видеопамять** (2)</span><span class="sxs-lookup"><span data-stu-id="38848-183">**VRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="38848-184">**DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="38848-184">**DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="38848-185">**SRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="38848-185">**SRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="38848-186">**Врам** (5)</span><span class="sxs-lookup"><span data-stu-id="38848-186">**WRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="38848-187">**Эдо ОЗУ** (6)</span><span class="sxs-lookup"><span data-stu-id="38848-187">**EDO RAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="38848-188">**Пакетная синхронная DRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="38848-188">**Burst Synchronous DRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="38848-189">**Конвейерный пакет SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="38848-189">**Pipelined Burst SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="38848-190">**Кдрам** (9)</span><span class="sxs-lookup"><span data-stu-id="38848-190">**CDRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="38848-191">**3DRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="38848-191">**3DRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="38848-192">**SDRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="38848-192">**SDRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="38848-193">**Сграм** (12)</span><span class="sxs-lookup"><span data-stu-id="38848-193">**SGRAM** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38848-194">**видеопроцессор**</span><span class="sxs-lookup"><span data-stu-id="38848-194">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38848-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38848-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38848-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38848-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38848-197">Текстовое описание процессора или контроллера видео.</span><span class="sxs-lookup"><span data-stu-id="38848-197">A text description of the video processor/controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38848-198">Требования</span><span class="sxs-lookup"><span data-stu-id="38848-198">Requirements</span></span>



| <span data-ttu-id="38848-199">Требование</span><span class="sxs-lookup"><span data-stu-id="38848-199">Requirement</span></span> | <span data-ttu-id="38848-200">Значение</span><span class="sxs-lookup"><span data-stu-id="38848-200">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38848-201">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38848-201">Minimum supported client</span></span><br/> | <span data-ttu-id="38848-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="38848-202">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="38848-203">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38848-203">Minimum supported server</span></span><br/> | <span data-ttu-id="38848-204">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38848-204">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="38848-205">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38848-205">Namespace</span></span><br/>                | <span data-ttu-id="38848-206">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="38848-206">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="38848-207">MOF</span><span class="sxs-lookup"><span data-stu-id="38848-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38848-208"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38848-208"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38848-209">DLL</span><span class="sxs-lookup"><span data-stu-id="38848-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38848-210"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38848-210"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="38848-211">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38848-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38848-212">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="38848-212">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

