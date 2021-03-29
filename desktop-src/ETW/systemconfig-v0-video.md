---
description: Этот класс является классом типа событий для событий конфигурации видео.
ms.assetid: 06aab3a3-a55e-4eb8-897a-2ad8349e5900
title: Класс SystemConfig_V0_Video
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Video
- SystemConfig_V0_Video.MemorySize
- SystemConfig_V0_Video.XResolution
- SystemConfig_V0_Video.YResolution
- SystemConfig_V0_Video.BitsPerPixel
- SystemConfig_V0_Video.VRefresh
- SystemConfig_V0_Video.ChipType
- SystemConfig_V0_Video.DACType
- SystemConfig_V0_Video.AdapterString
- SystemConfig_V0_Video.BiosString
- SystemConfig_V0_Video.DeviceId
- SystemConfig_V0_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: b840e3c06e74f8acbd1e43550559385e78c9a638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985097"
---
# <a name="systemconfig_v0_video-class"></a><span data-ttu-id="c7b90-103">\_ \_ Класс видео системконфиг v0</span><span class="sxs-lookup"><span data-stu-id="c7b90-103">SystemConfig\_V0\_Video class</span></span>

<span data-ttu-id="c7b90-104">Этот класс является классом типа событий для событий конфигурации видео.</span><span class="sxs-lookup"><span data-stu-id="c7b90-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="c7b90-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="c7b90-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7b90-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7b90-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_V0_Video : SystemConfig_V0
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

## <a name="members"></a><span data-ttu-id="c7b90-107">Участники</span><span class="sxs-lookup"><span data-stu-id="c7b90-107">Members</span></span>

<span data-ttu-id="c7b90-108">Класс **\_ \_ видео системконфиг v0** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c7b90-108">The **SystemConfig\_V0\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="c7b90-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c7b90-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7b90-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c7b90-110">Properties</span></span>

<span data-ttu-id="c7b90-111">Класс **\_ \_ видео системконфиг v0** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c7b90-111">The **SystemConfig\_V0\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7b90-112">**адаптерстринг**</span><span class="sxs-lookup"><span data-stu-id="c7b90-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b90-113">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="c7b90-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7b90-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-115">Квалификаторы: **вмидатаид** (8), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="c7b90-115">Qualifiers: **WmiDataId** (8), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7b90-116">Имя или описание адаптера.</span><span class="sxs-lookup"><span data-stu-id="c7b90-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c7b90-117">**биосстринг**</span><span class="sxs-lookup"><span data-stu-id="c7b90-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b90-118">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="c7b90-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7b90-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-120">Квалификаторы: **вмидатаид** (9), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="c7b90-120">Qualifiers: **WmiDataId** (9), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7b90-121">Имя BIOS адаптера.</span><span class="sxs-lookup"><span data-stu-id="c7b90-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c7b90-122">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="c7b90-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b90-123">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b90-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7b90-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-125">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="c7b90-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="c7b90-126">Число битов, используемых для вывода каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="c7b90-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="c7b90-127">**чиптипе**</span><span class="sxs-lookup"><span data-stu-id="c7b90-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b90-128">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="c7b90-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7b90-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-130">Квалификаторы: **вмидатаид** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="c7b90-130">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7b90-131">Имя микросхемы адаптера.</span><span class="sxs-lookup"><span data-stu-id="c7b90-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c7b90-132">**DACType**</span><span class="sxs-lookup"><span data-stu-id="c7b90-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b90-133">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="c7b90-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7b90-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-135">Квалификаторы: **вмидатаид** (7), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="c7b90-135">Qualifiers: **WmiDataId** (7), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7b90-136">Имя микросхемы цифрового преобразователя (DAC) адаптера.</span><span class="sxs-lookup"><span data-stu-id="c7b90-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c7b90-137">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="c7b90-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b90-138">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="c7b90-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7b90-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-140">Квалификаторы: **вмидатаид** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="c7b90-140">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7b90-141">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c7b90-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="c7b90-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="c7b90-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b90-143">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b90-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7b90-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-145">Квалификаторы: **вмидатаид** (1)</span><span class="sxs-lookup"><span data-stu-id="c7b90-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="c7b90-146">Максимальный поддерживаемый объем памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="c7b90-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c7b90-147">**статефлагс**</span><span class="sxs-lookup"><span data-stu-id="c7b90-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b90-148">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b90-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7b90-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-150">Квалификаторы: **вмидатаид** (11)</span><span class="sxs-lookup"><span data-stu-id="c7b90-150">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="c7b90-151">Флаги состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="c7b90-151">Device state flags.</span></span> <span data-ttu-id="c7b90-152">Это может быть любое разумное сочетание следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="c7b90-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="c7b90-153">Значение</span><span class="sxs-lookup"><span data-stu-id="c7b90-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="c7b90-154">Значение</span><span class="sxs-lookup"><span data-stu-id="c7b90-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="c7b90-155"><dt>**Отображение \_ УСТРОЙСТВО \_ , подключенное \_ к \_ рабочему столу**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b90-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="c7b90-156">Устройство является частью рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="c7b90-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="c7b90-157"><dt>**Отображение \_ \_ \_ Драйвер зеркального отображения устройств**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b90-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="c7b90-158">Представляет псевдо-устройство, используемое для отражения прорисовки приложения для подключения к удаленному компьютеру или другим целям.</span><span class="sxs-lookup"><span data-stu-id="c7b90-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="c7b90-159">С этим устройством связан невидимый псевдо-монитор.</span><span class="sxs-lookup"><span data-stu-id="c7b90-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="c7b90-160">Например, NetMeeting использует его.</span><span class="sxs-lookup"><span data-stu-id="c7b90-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="c7b90-161"><dt>**Отображение \_ \_МОДЕСПРУНЕД устройства**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b90-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="c7b90-162">Устройство имеет больше режимов вывода, чем поддерживается устройствами вывода.</span><span class="sxs-lookup"><span data-stu-id="c7b90-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="c7b90-163"><dt>**Отображение \_ \_Основное \_ устройство**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b90-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="c7b90-164">Основной рабочий стол находится на устройстве.</span><span class="sxs-lookup"><span data-stu-id="c7b90-164">The primary desktop is on the device.</span></span> <span data-ttu-id="c7b90-165">Для системы с одной картой экрана всегда устанавливается значение.</span><span class="sxs-lookup"><span data-stu-id="c7b90-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="c7b90-166">Для системы с несколькими экранными картами этот набор может иметь только одно устройство.</span><span class="sxs-lookup"><span data-stu-id="c7b90-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="c7b90-167"><dt>**Отображение \_ \_Съемное устройство**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b90-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="c7b90-168">Устройство является съемным; Он не может быть основным дисплеем.</span><span class="sxs-lookup"><span data-stu-id="c7b90-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="c7b90-169"><dt>**Отображение \_ \_ \_ Совместимость устройства VGA**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b90-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="c7b90-170">Устройство совместимо с VGA.</span><span class="sxs-lookup"><span data-stu-id="c7b90-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="c7b90-171">**врефреш**</span><span class="sxs-lookup"><span data-stu-id="c7b90-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b90-172">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b90-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7b90-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-174">Квалификаторы: **вмидатаид** (5)</span><span class="sxs-lookup"><span data-stu-id="c7b90-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="c7b90-175">Текущая частота обновления в герцах.</span><span class="sxs-lookup"><span data-stu-id="c7b90-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="c7b90-176">**ксресолутион**</span><span class="sxs-lookup"><span data-stu-id="c7b90-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b90-177">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b90-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7b90-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-179">Квалификаторы: **вмидатаид** (2)</span><span class="sxs-lookup"><span data-stu-id="c7b90-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="c7b90-180">Текущее число точек по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="c7b90-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="c7b90-181">**иресолутион**</span><span class="sxs-lookup"><span data-stu-id="c7b90-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7b90-182">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7b90-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7b90-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7b90-184">Квалификаторы: **вмидатаид** (3)</span><span class="sxs-lookup"><span data-stu-id="c7b90-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="c7b90-185">Текущее число пикселей по вертикали.</span><span class="sxs-lookup"><span data-stu-id="c7b90-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7b90-186">Требования</span><span class="sxs-lookup"><span data-stu-id="c7b90-186">Requirements</span></span>



| <span data-ttu-id="c7b90-187">Требование</span><span class="sxs-lookup"><span data-stu-id="c7b90-187">Requirement</span></span> | <span data-ttu-id="c7b90-188">Значение</span><span class="sxs-lookup"><span data-stu-id="c7b90-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c7b90-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7b90-189">Minimum supported client</span></span><br/> | <span data-ttu-id="c7b90-190">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c7b90-190">None supported</span></span><br/>                            |
| <span data-ttu-id="c7b90-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7b90-191">Minimum supported server</span></span><br/> | <span data-ttu-id="c7b90-192">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7b90-192">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7b90-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7b90-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b90-194">**Системконфиг \_ v0**</span><span class="sxs-lookup"><span data-stu-id="c7b90-194">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




