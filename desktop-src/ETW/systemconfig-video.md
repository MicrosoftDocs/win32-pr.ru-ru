---
description: Этот класс является классом типа событий для событий конфигурации видео.
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: Класс SystemConfig_Video
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 370c67501b75f0fd4ac88488744280f1e0065bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986132"
---
# <a name="systemconfig_video-class"></a><span data-ttu-id="14a24-103">\_Класс видео системконфиг</span><span class="sxs-lookup"><span data-stu-id="14a24-103">SystemConfig\_Video class</span></span>

<span data-ttu-id="14a24-104">Этот класс является классом типа событий для событий конфигурации видео.</span><span class="sxs-lookup"><span data-stu-id="14a24-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="14a24-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="14a24-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a24-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14a24-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a><span data-ttu-id="14a24-107">Участники</span><span class="sxs-lookup"><span data-stu-id="14a24-107">Members</span></span>

<span data-ttu-id="14a24-108">Класс **\_ видео системконфиг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="14a24-108">The **SystemConfig\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="14a24-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="14a24-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14a24-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="14a24-110">Properties</span></span>

<span data-ttu-id="14a24-111">Класс **\_ Video системконфиг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="14a24-111">The **SystemConfig\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14a24-112">**адаптерстринг**</span><span class="sxs-lookup"><span data-stu-id="14a24-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a24-113">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="14a24-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="14a24-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="14a24-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a24-115">Квалификаторы: **вмидатаид** (8), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="14a24-115">Qualifiers: **WmiDataId** (8), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="14a24-116">Имя или описание адаптера.</span><span class="sxs-lookup"><span data-stu-id="14a24-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="14a24-117">**биосстринг**</span><span class="sxs-lookup"><span data-stu-id="14a24-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a24-118">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="14a24-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="14a24-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="14a24-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a24-120">Квалификаторы: **вмидатаид** (9), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="14a24-120">Qualifiers: **WmiDataId** (9), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="14a24-121">Имя BIOS адаптера.</span><span class="sxs-lookup"><span data-stu-id="14a24-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="14a24-122">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="14a24-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a24-123">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a24-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a24-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="14a24-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a24-125">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="14a24-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="14a24-126">Число битов, используемых для вывода каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="14a24-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="14a24-127">**чиптипе**</span><span class="sxs-lookup"><span data-stu-id="14a24-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a24-128">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="14a24-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="14a24-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="14a24-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a24-130">Квалификаторы: **вмидатаид** (6), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="14a24-130">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="14a24-131">Имя микросхемы адаптера.</span><span class="sxs-lookup"><span data-stu-id="14a24-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="14a24-132">**DACType**</span><span class="sxs-lookup"><span data-stu-id="14a24-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a24-133">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="14a24-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="14a24-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="14a24-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a24-135">Квалификаторы: **вмидатаид** (7), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="14a24-135">Qualifiers: **WmiDataId** (7), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="14a24-136">Имя микросхемы цифрового преобразователя (DAC) адаптера.</span><span class="sxs-lookup"><span data-stu-id="14a24-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="14a24-137">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="14a24-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a24-138">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="14a24-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="14a24-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="14a24-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a24-140">Квалификаторы: **вмидатаид** (10), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="14a24-140">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="14a24-141">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="14a24-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="14a24-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="14a24-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a24-143">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a24-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a24-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="14a24-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a24-145">Квалификаторы: **вмидатаид** (1)</span><span class="sxs-lookup"><span data-stu-id="14a24-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="14a24-146">Максимальный поддерживаемый объем памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="14a24-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="14a24-147">**статефлагс**</span><span class="sxs-lookup"><span data-stu-id="14a24-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a24-148">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a24-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a24-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="14a24-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a24-150">Квалификаторы: **вмидатаид** (11), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="14a24-150">Qualifiers: **WmiDataId** (11), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="14a24-151">Флаги состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="14a24-151">Device state flags.</span></span> <span data-ttu-id="14a24-152">Это может быть любое разумное сочетание следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="14a24-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="14a24-153">Значение</span><span class="sxs-lookup"><span data-stu-id="14a24-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="14a24-154">Значение</span><span class="sxs-lookup"><span data-stu-id="14a24-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="14a24-155"><dt>**Отображение \_ УСТРОЙСТВО \_ , подключенное \_ к \_ рабочему столу**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="14a24-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="14a24-156">Устройство является частью рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="14a24-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="14a24-157"><dt>**Отображение \_ \_ \_ Драйвер зеркального отображения устройств**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="14a24-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="14a24-158">Представляет псевдо-устройство, используемое для отражения прорисовки приложения для подключения к удаленному компьютеру или другим целям.</span><span class="sxs-lookup"><span data-stu-id="14a24-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="14a24-159">С этим устройством связан невидимый псевдо-монитор.</span><span class="sxs-lookup"><span data-stu-id="14a24-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="14a24-160">Например, NetMeeting использует его.</span><span class="sxs-lookup"><span data-stu-id="14a24-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="14a24-161"><dt>**Отображение \_ \_МОДЕСПРУНЕД устройства**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="14a24-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="14a24-162">Устройство имеет больше режимов вывода, чем поддерживается устройствами вывода.</span><span class="sxs-lookup"><span data-stu-id="14a24-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="14a24-163"><dt>**Отображение \_ \_Основное \_ устройство**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="14a24-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="14a24-164">Основной рабочий стол находится на устройстве.</span><span class="sxs-lookup"><span data-stu-id="14a24-164">The primary desktop is on the device.</span></span> <span data-ttu-id="14a24-165">Для системы с одной картой экрана всегда устанавливается значение.</span><span class="sxs-lookup"><span data-stu-id="14a24-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="14a24-166">Для системы с несколькими экранными картами этот набор может иметь только одно устройство.</span><span class="sxs-lookup"><span data-stu-id="14a24-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="14a24-167"><dt>**Отображение \_ \_Съемное устройство**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="14a24-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="14a24-168">Устройство является съемным; Он не может быть основным дисплеем.</span><span class="sxs-lookup"><span data-stu-id="14a24-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="14a24-169"><dt>**Отображение \_ \_ \_ Совместимость устройства VGA**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="14a24-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="14a24-170">Устройство совместимо с VGA.</span><span class="sxs-lookup"><span data-stu-id="14a24-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="14a24-171">**врефреш**</span><span class="sxs-lookup"><span data-stu-id="14a24-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a24-172">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a24-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a24-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="14a24-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a24-174">Квалификаторы: **вмидатаид** (5)</span><span class="sxs-lookup"><span data-stu-id="14a24-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="14a24-175">Текущая частота обновления в герцах.</span><span class="sxs-lookup"><span data-stu-id="14a24-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="14a24-176">**ксресолутион**</span><span class="sxs-lookup"><span data-stu-id="14a24-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a24-177">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a24-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a24-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="14a24-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a24-179">Квалификаторы: **вмидатаид** (2)</span><span class="sxs-lookup"><span data-stu-id="14a24-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="14a24-180">Текущее число точек по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="14a24-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="14a24-181">**иресолутион**</span><span class="sxs-lookup"><span data-stu-id="14a24-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14a24-182">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14a24-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14a24-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="14a24-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14a24-184">Квалификаторы: **вмидатаид** (3)</span><span class="sxs-lookup"><span data-stu-id="14a24-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="14a24-185">Текущее число пикселей по вертикали.</span><span class="sxs-lookup"><span data-stu-id="14a24-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14a24-186">Требования</span><span class="sxs-lookup"><span data-stu-id="14a24-186">Requirements</span></span>



| <span data-ttu-id="14a24-187">Требование</span><span class="sxs-lookup"><span data-stu-id="14a24-187">Requirement</span></span> | <span data-ttu-id="14a24-188">Значение</span><span class="sxs-lookup"><span data-stu-id="14a24-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14a24-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14a24-189">Minimum supported client</span></span><br/> | <span data-ttu-id="14a24-190">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14a24-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="14a24-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14a24-191">Minimum supported server</span></span><br/> | <span data-ttu-id="14a24-192">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14a24-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14a24-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14a24-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a24-194">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="14a24-194">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




