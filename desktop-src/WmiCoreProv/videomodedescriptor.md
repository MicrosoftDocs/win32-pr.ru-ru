---
description: Содержит элементы дескриптора режима для массива Мониторсаурцемодес в классе Вмимониторлистедсуппортедсаурцемодес.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: Класс Видеомодедескриптор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 06094b24b6b8197eab89b65cd5a9a83f46b39f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348425"
---
# <a name="videomodedescriptor-class"></a><span data-ttu-id="982d3-103">Класс Видеомодедескриптор</span><span class="sxs-lookup"><span data-stu-id="982d3-103">VideoModeDescriptor class</span></span>

<span data-ttu-id="982d3-104">Класс WMI **видеомодедескрипторвидео** содержит элементы дескриптора режима для массива **Мониторсаурцемодес** в классе [**вмимониторлистедсуппортедсаурцемодес**](wmimonitorlistedsupportedsourcemodes.md) .</span><span class="sxs-lookup"><span data-stu-id="982d3-104">The **VideoModeDescriptorVideo** WMI class contains mode descriptor elements for the **MonitorSourceModes** array in the [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) class.</span></span> <span data-ttu-id="982d3-105">Эти элементы включают в себя такие функции мониторинга, как частота обновления, характеристики пикселя или размер изображения.</span><span class="sxs-lookup"><span data-stu-id="982d3-105">These elements include monitor features such as refresh rate, pixel characteristics, or image size.</span></span> <span data-ttu-id="982d3-106">Класс **видеомодедескрипторвидео** содержит сведения, которые являются надмножеством данных, доступных из установленных, стандартных и подробных временных блоков.</span><span class="sxs-lookup"><span data-stu-id="982d3-106">The **VideoModeDescriptorVideo** class contains information that is a superset of the data available from established, standard, and detailed timing blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="982d3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="982d3-107">Syntax</span></span>

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a><span data-ttu-id="982d3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="982d3-108">Members</span></span>

<span data-ttu-id="982d3-109">Класс **видеомодедескриптор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="982d3-109">The **VideoModeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="982d3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="982d3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="982d3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="982d3-111">Properties</span></span>

<span data-ttu-id="982d3-112">Класс **видеомодедескриптор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="982d3-112">The **VideoModeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="982d3-113">**компоситеполарититипе**</span><span class="sxs-lookup"><span data-stu-id="982d3-113">**CompositePolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-114">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="982d3-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-116">Тип составной полярности.</span><span class="sxs-lookup"><span data-stu-id="982d3-116">Composite polarity type.</span></span> <span data-ttu-id="982d3-117">Это Полярность импульсов горизонтальной синхронизации за пределами вертикальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="982d3-117">This is polarity of horizontal sync pulses outside of vertical sync.</span></span>



| <span data-ttu-id="982d3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-118">Value</span></span>                                                                              | <span data-ttu-id="982d3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-119">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="982d3-120"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-120"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="982d3-121">Составная полярность положительна.</span><span class="sxs-lookup"><span data-stu-id="982d3-121">Composite polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="982d3-122"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-122"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="982d3-123">Составная полярность является отрицательной.</span><span class="sxs-lookup"><span data-stu-id="982d3-123">Composite polarity is negative.</span></span><br/>                                 |
| <dl> <span data-ttu-id="982d3-124"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-124"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="982d3-125">Не применяется</span><span class="sxs-lookup"><span data-stu-id="982d3-125">Not applicable.</span></span> <span data-ttu-id="982d3-126">Тип синхронизации сигнала должен быть цифровым составным.</span><span class="sxs-lookup"><span data-stu-id="982d3-126">The signal sync type must be digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="982d3-127">**хоризонталактивепикселс**</span><span class="sxs-lookup"><span data-stu-id="982d3-127">**HorizontalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-128">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-130">Количество горизонтально активных пикселей.</span><span class="sxs-lookup"><span data-stu-id="982d3-130">Number of horizontally active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-131">**хоризонталбланкингпикселс**</span><span class="sxs-lookup"><span data-stu-id="982d3-131">**HorizontalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-132">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-134">Число горизонтальных пустых пикселей</span><span class="sxs-lookup"><span data-stu-id="982d3-134">Number of horizontally blanking pixels</span></span>

</dd> <dt>

<span data-ttu-id="982d3-135">**хоризонталбордер**</span><span class="sxs-lookup"><span data-stu-id="982d3-135">**HorizontalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-136">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-138">Горизонтальная граница.</span><span class="sxs-lookup"><span data-stu-id="982d3-138">Horizontal border.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-139">**хоризонталимажесизе**</span><span class="sxs-lookup"><span data-stu-id="982d3-139">**HorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-140">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-142">Горизонтальный размер изображения в миллиметрах (мм).</span><span class="sxs-lookup"><span data-stu-id="982d3-142">Horizontal image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="982d3-143">**хоризонталполарититипе**</span><span class="sxs-lookup"><span data-stu-id="982d3-143">**HorizontalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-144">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="982d3-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-146">Тип горизонтальной полярности.</span><span class="sxs-lookup"><span data-stu-id="982d3-146">Horizontal polarity type.</span></span>



| <span data-ttu-id="982d3-147">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-147">Value</span></span>                                                                              | <span data-ttu-id="982d3-148">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-148">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="982d3-149"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-149"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="982d3-150">Горизонтальная полярность является положительной.</span><span class="sxs-lookup"><span data-stu-id="982d3-150">Horizontal polarity is positive.</span></span><br/>                               |
| <dl> <span data-ttu-id="982d3-151"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-151"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="982d3-152">Горизонтальная полярность является отрицательной.</span><span class="sxs-lookup"><span data-stu-id="982d3-152">Horizontal polarity is negative.</span></span><br/>                               |
| <dl> <span data-ttu-id="982d3-153"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-153"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="982d3-154">Не применяется</span><span class="sxs-lookup"><span data-stu-id="982d3-154">Not applicable.</span></span> <span data-ttu-id="982d3-155">Тип синхронизации сигнала должен быть цифровым отделением.</span><span class="sxs-lookup"><span data-stu-id="982d3-155">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="982d3-156">**хоризонталрефрешратеденоминатор**</span><span class="sxs-lookup"><span data-stu-id="982d3-156">**HorizontalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-157">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-159">Знаменатель частоты обновления по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="982d3-159">Horizontal refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-160">**хоризонталрефрешратенумератор**</span><span class="sxs-lookup"><span data-stu-id="982d3-160">**HorizontalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-161">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-163">Числитель частоты обновления по горизонтали в герцах (Гц).</span><span class="sxs-lookup"><span data-stu-id="982d3-163">Horizontal refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="982d3-164">**хоризонталсинкоффсет**</span><span class="sxs-lookup"><span data-stu-id="982d3-164">**HorizontalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-165">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-167">Смещение горизонтальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="982d3-167">Horizontal sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-168">**хоризонталсинкпулсевидс**</span><span class="sxs-lookup"><span data-stu-id="982d3-168">**HorizontalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-169">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-171">Ширина импульса горизонтальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="982d3-171">Horizontal sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-172">**С чередованием**</span><span class="sxs-lookup"><span data-stu-id="982d3-172">**IsInterlaced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-173">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="982d3-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-175">Указывает, является ли режим просмотра чередованием.</span><span class="sxs-lookup"><span data-stu-id="982d3-175">Indicates whether the display mode is interlaced.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-176">**иссерратионрекуиред**</span><span class="sxs-lookup"><span data-stu-id="982d3-176">**IsSerrationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-177">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="982d3-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-179">Указывает, какой тип серратион требуется при необходимости.</span><span class="sxs-lookup"><span data-stu-id="982d3-179">Indicates what type of serration is required, if appropriate.</span></span>



| <span data-ttu-id="982d3-180">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-180">Value</span></span>                                                                              | <span data-ttu-id="982d3-181">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-181">Meaning</span></span>                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="982d3-182"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="982d3-183">Контроллер должен предоставлять горизонтальную синхронизацию во время вертикальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="982d3-183">Controller shall supply horizontal sync during vertical sync.</span></span><br/>                                 |
| <dl> <span data-ttu-id="982d3-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="982d3-185">Контроллер не должен предоставлять горизонтальную синхронизацию во время вертикальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="982d3-185">Controller shall not supply horizontal sync during vertical sync.</span></span><br/>                             |
| <dl> <span data-ttu-id="982d3-186"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-186"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="982d3-187">Не применяется</span><span class="sxs-lookup"><span data-stu-id="982d3-187">Not applicable.</span></span> <span data-ttu-id="982d3-188">Тип синхронизации сигнала должен быть биполар, аналоговым составным или цифровым составным.</span><span class="sxs-lookup"><span data-stu-id="982d3-188">The signal sync type must be bipolar, analog composite, or digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="982d3-189">**иссинконргб**</span><span class="sxs-lookup"><span data-stu-id="982d3-189">**IsSyncOnRGB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-190">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="982d3-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-192">Указывает, какие строки видеосигнала должны быть синхронизированы, если это уместно.</span><span class="sxs-lookup"><span data-stu-id="982d3-192">Indicates which video signal lines should be synchronized, if appropriate.</span></span>



| <span data-ttu-id="982d3-193">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-193">Value</span></span>                                                                              | <span data-ttu-id="982d3-194">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-194">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="982d3-195"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-195"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="982d3-196">Пульс синхронизации должен отображаться на всех трех строках видеосигнала.</span><span class="sxs-lookup"><span data-stu-id="982d3-196">Sync pulse should appear on all 3 video signal lines.</span></span><br/>                  |
| <dl> <span data-ttu-id="982d3-197"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-197"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="982d3-198">Импульс синхронизации должен отображаться только в линии зеленого сигнала.</span><span class="sxs-lookup"><span data-stu-id="982d3-198">Sync pulse should only appear on the green video signal line.</span></span><br/>          |
| <dl> <span data-ttu-id="982d3-199"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-199"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="982d3-200">Не применяется</span><span class="sxs-lookup"><span data-stu-id="982d3-200">Not applicable.</span></span> <span data-ttu-id="982d3-201">Тип синхронизации сигнала должен быть биполар аналоговым составным.</span><span class="sxs-lookup"><span data-stu-id="982d3-201">The signal sync type must be bipolar analog composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="982d3-202">**пикселклоккрате**</span><span class="sxs-lookup"><span data-stu-id="982d3-202">**PixelClockRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-203">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="982d3-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-205">Частота часов в пикселях в герцах (Гц).</span><span class="sxs-lookup"><span data-stu-id="982d3-205">Pixel clock rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="982d3-206">**стереомодетипе**</span><span class="sxs-lookup"><span data-stu-id="982d3-206">**StereoModeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-207">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="982d3-207">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-209">Тип стерео.</span><span class="sxs-lookup"><span data-stu-id="982d3-209">Stereo mode type.</span></span> <span data-ttu-id="982d3-210">В следующей таблице перечислены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="982d3-210">The following table lists the possible values.</span></span>



| <span data-ttu-id="982d3-211">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-211">Value</span></span>                                                                              | <span data-ttu-id="982d3-212">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-212">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="982d3-213"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-213"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="982d3-214">Нет стерео.</span><span class="sxs-lookup"><span data-stu-id="982d3-214">No stereo.</span></span><br/>                                               |
| <dl> <span data-ttu-id="982d3-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-215"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="982d3-216">Поле последовательного стерео с изображением справа для стерео синхронизации.</span><span class="sxs-lookup"><span data-stu-id="982d3-216">Field sequential stereo with right image on stereo sync.</span></span><br/> |
| <dl> <span data-ttu-id="982d3-217"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-217"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="982d3-218">Поле последовательного стерео с изображением слева на странице "стерео Sync".</span><span class="sxs-lookup"><span data-stu-id="982d3-218">Field sequential stereo with left image on stereo sync.</span></span><br/>  |
| <dl> <span data-ttu-id="982d3-219"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-219"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="982d3-220">Двусторонняя чередование с изображением справа, находящегося на четных линиях.</span><span class="sxs-lookup"><span data-stu-id="982d3-220">2-way Interleaved Stereo with Right Image on Even Lines.</span></span><br/> |
| <dl> <span data-ttu-id="982d3-221"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-221"><dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="982d3-222">Двусторонняя чередующийся стерео с изображением левого размера на четных строках.</span><span class="sxs-lookup"><span data-stu-id="982d3-222">2-way Interleaved Stereo with Left Image on Even Lines.</span></span><br/>  |
| <dl> <span data-ttu-id="982d3-223"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-223"><dt>5 (0x5)</dt></span></span> </dl> | <span data-ttu-id="982d3-224">4-факторный стерео с чередованием.</span><span class="sxs-lookup"><span data-stu-id="982d3-224">4-way Interleaved Stereo.</span></span><br/>                                |
| <dl> <span data-ttu-id="982d3-225"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-225"><dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="982d3-226">Параллельное стерео чередование.</span><span class="sxs-lookup"><span data-stu-id="982d3-226">Side-by-Side Interleaved Stereo.</span></span><br/>                         |



 

</dd> <dt>

<span data-ttu-id="982d3-227">**синксигналтипе**</span><span class="sxs-lookup"><span data-stu-id="982d3-227">**SyncSignalType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-228">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="982d3-228">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-230">Тип синхронизации сигнала.</span><span class="sxs-lookup"><span data-stu-id="982d3-230">Signal sync type.</span></span> <span data-ttu-id="982d3-231">В следующей таблице перечислены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="982d3-231">The following table lists the possible values.</span></span>



| <span data-ttu-id="982d3-232">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-232">Value</span></span>                                                                              | <span data-ttu-id="982d3-233">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-233">Meaning</span></span>                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="982d3-234"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-234"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="982d3-235">Аналоговый составной</span><span class="sxs-lookup"><span data-stu-id="982d3-235">Analog Composite</span></span><br/>         |
| <dl> <span data-ttu-id="982d3-236"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-236"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="982d3-237">Биполар аналоговый составной</span><span class="sxs-lookup"><span data-stu-id="982d3-237">Bipolar Analog Composite</span></span><br/> |
| <dl> <span data-ttu-id="982d3-238"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-238"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="982d3-239">Цифровое составное</span><span class="sxs-lookup"><span data-stu-id="982d3-239">Digital Composite</span></span><br/>        |
| <dl> <span data-ttu-id="982d3-240"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-240"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="982d3-241">Цифровая отдельная</span><span class="sxs-lookup"><span data-stu-id="982d3-241">Digital Separate</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="982d3-242">**вертикалактивепикселс**</span><span class="sxs-lookup"><span data-stu-id="982d3-242">**VerticalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-243">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-245">Количество активных пикселей по вертикали.</span><span class="sxs-lookup"><span data-stu-id="982d3-245">Number of vertically active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-246">**вертикалбланкингпикселс**</span><span class="sxs-lookup"><span data-stu-id="982d3-246">**VerticalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-247">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-249">Количество пустых пикселей по вертикали.</span><span class="sxs-lookup"><span data-stu-id="982d3-249">Number of vertically blanking pixels.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-250">**вертикалбордер**</span><span class="sxs-lookup"><span data-stu-id="982d3-250">**VerticalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-251">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-253">Вертикальная граница.</span><span class="sxs-lookup"><span data-stu-id="982d3-253">Vertical border.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-254">**вертикалимажесизе**</span><span class="sxs-lookup"><span data-stu-id="982d3-254">**VerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-255">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-257">Размер вертикального изображения в миллиметрах (мм).</span><span class="sxs-lookup"><span data-stu-id="982d3-257">Vertical image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="982d3-258">**вертикалполарититипе**</span><span class="sxs-lookup"><span data-stu-id="982d3-258">**VerticalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-259">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="982d3-259">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-261">Тип вертикальной полярности.</span><span class="sxs-lookup"><span data-stu-id="982d3-261">Vertical polarity type.</span></span>



| <span data-ttu-id="982d3-262">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-262">Value</span></span>                                                                              | <span data-ttu-id="982d3-263">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-263">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="982d3-264"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-264"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="982d3-265">Вертикальная полярность положительная.</span><span class="sxs-lookup"><span data-stu-id="982d3-265">Vertical polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="982d3-266"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-266"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="982d3-267">Вертикальная полярность отрицательна</span><span class="sxs-lookup"><span data-stu-id="982d3-267">Vertical polarity is negative</span></span><br/>                                  |
| <dl> <span data-ttu-id="982d3-268"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-268"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="982d3-269">Не применяется</span><span class="sxs-lookup"><span data-stu-id="982d3-269">Not applicable.</span></span> <span data-ttu-id="982d3-270">Тип синхронизации сигнала должен быть цифровым отделением.</span><span class="sxs-lookup"><span data-stu-id="982d3-270">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="982d3-271">**вертикалрефрешратеденоминатор**</span><span class="sxs-lookup"><span data-stu-id="982d3-271">**VerticalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-272">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-274">Знаменатель частоты обновления по вертикали.</span><span class="sxs-lookup"><span data-stu-id="982d3-274">Vertical refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-275">**вертикалрефрешратенумератор**</span><span class="sxs-lookup"><span data-stu-id="982d3-275">**VerticalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-276">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-278">Числитель частоты обновления по вертикали в герцах (Гц).</span><span class="sxs-lookup"><span data-stu-id="982d3-278">Vertical refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="982d3-279">**вертикалсинкоффсет**</span><span class="sxs-lookup"><span data-stu-id="982d3-279">**VerticalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-280">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-282">Смещение вертикальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="982d3-282">Vertical sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-283">**вертикалсинкпулсевидс**</span><span class="sxs-lookup"><span data-stu-id="982d3-283">**VerticalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-284">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="982d3-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-286">Ширина импульса вертикальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="982d3-286">Vertical sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="982d3-287">видеостандардтипе</span><span class="sxs-lookup"><span data-stu-id="982d3-287">VideoStandardType</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="982d3-288">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="982d3-288">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="982d3-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="982d3-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="982d3-290">Стандартный тип видео.</span><span class="sxs-lookup"><span data-stu-id="982d3-290">Video standard type.</span></span>



| <span data-ttu-id="982d3-291">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-291">Value</span></span>                                                                                | <span data-ttu-id="982d3-292">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-292">Meaning</span></span>                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="982d3-293"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-293"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="982d3-294">Другое</span><span class="sxs-lookup"><span data-stu-id="982d3-294">Other</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="982d3-295"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-295"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="982d3-296">VESA ДМТ.</span><span class="sxs-lookup"><span data-stu-id="982d3-296">VESA DMT.</span></span> <span data-ttu-id="982d3-297">Из спецификации отображения сведений о времени монитора для дисплея по стандарту видео (VESA).</span><span class="sxs-lookup"><span data-stu-id="982d3-297">From Video Electronics Standard Association (VESA) Display Monitor Timings specification.</span></span><br/> |
| <dl> <span data-ttu-id="982d3-298"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-298"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="982d3-299">VESA ГТФ.</span><span class="sxs-lookup"><span data-stu-id="982d3-299">VESA GTF.</span></span> <span data-ttu-id="982d3-300">Из стандарта VESA обобщенной формулы расчета времени.</span><span class="sxs-lookup"><span data-stu-id="982d3-300">From VESA Generalized Timing Formula standard.</span></span><br/>                                            |
| <dl> <span data-ttu-id="982d3-301"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-301"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="982d3-302">Стандартный режим видео VESA CVT/от VESA.</span><span class="sxs-lookup"><span data-stu-id="982d3-302">VESA CVT/ From VESA Coordinated Video Timings standard.</span></span><br/>                                             |
| <dl> <span data-ttu-id="982d3-303"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-303"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="982d3-304">IBM</span><span class="sxs-lookup"><span data-stu-id="982d3-304">IBM</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="982d3-305"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-305"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="982d3-306">КЛИЕНТАМ</span><span class="sxs-lookup"><span data-stu-id="982d3-306">APPLE</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="982d3-307"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-307"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="982d3-308">NTSC M</span><span class="sxs-lookup"><span data-stu-id="982d3-308">NTSC M</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="982d3-309"><dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-309"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="982d3-310">NTSC J</span><span class="sxs-lookup"><span data-stu-id="982d3-310">NTSC J</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="982d3-311"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-311"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="982d3-312">NTSC 433</span><span class="sxs-lookup"><span data-stu-id="982d3-312">NTSC 433</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="982d3-313"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-313"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="982d3-314">PAL B</span><span class="sxs-lookup"><span data-stu-id="982d3-314">PAL B</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="982d3-315"><dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-315"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="982d3-316">PAL B1</span><span class="sxs-lookup"><span data-stu-id="982d3-316">PAL B1</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="982d3-317"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-317"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="982d3-318">PAL G</span><span class="sxs-lookup"><span data-stu-id="982d3-318">PAL G</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="982d3-319"><dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-319"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="982d3-320">PAL H</span><span class="sxs-lookup"><span data-stu-id="982d3-320">PAL H</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="982d3-321"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-321"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="982d3-322">PAL I</span><span class="sxs-lookup"><span data-stu-id="982d3-322">PAL I</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="982d3-323"><dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-323"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="982d3-324">PAL D</span><span class="sxs-lookup"><span data-stu-id="982d3-324">PAL D</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="982d3-325"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-325"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="982d3-326">PAL N</span><span class="sxs-lookup"><span data-stu-id="982d3-326">PAL N</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="982d3-327"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-327"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="982d3-328">NC PAL</span><span class="sxs-lookup"><span data-stu-id="982d3-328">PAL NC</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="982d3-329"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-329"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="982d3-330">СЕКАМ Б</span><span class="sxs-lookup"><span data-stu-id="982d3-330">SECAM B</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="982d3-331"><dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-331"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="982d3-332">СЕКАМ Г</span><span class="sxs-lookup"><span data-stu-id="982d3-332">SECAM D</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="982d3-333"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-333"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="982d3-334">СЕКАМ G</span><span class="sxs-lookup"><span data-stu-id="982d3-334">SECAM G</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="982d3-335"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-335"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="982d3-336">СЕКАМ H</span><span class="sxs-lookup"><span data-stu-id="982d3-336">SECAM H</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="982d3-337"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-337"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="982d3-338">СЕКАМ Р</span><span class="sxs-lookup"><span data-stu-id="982d3-338">SECAM K</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="982d3-339"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-339"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="982d3-340">СЕКАМ K1</span><span class="sxs-lookup"><span data-stu-id="982d3-340">SECAM K1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="982d3-341"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-341"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="982d3-342">СЕКАМ L</span><span class="sxs-lookup"><span data-stu-id="982d3-342">SECAM L</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="982d3-343"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-343"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="982d3-344">СЕКАМ L1</span><span class="sxs-lookup"><span data-stu-id="982d3-344">SECAM L1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="982d3-345"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-345"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="982d3-346">EIA861</span><span class="sxs-lookup"><span data-stu-id="982d3-346">EIA861</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="982d3-347"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-347"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="982d3-348">EIA861A</span><span class="sxs-lookup"><span data-stu-id="982d3-348">EIA861A</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="982d3-349"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-349"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="982d3-350">EIA861B</span><span class="sxs-lookup"><span data-stu-id="982d3-350">EIA861B</span></span><br/>                                                                                             |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="982d3-351">Требования</span><span class="sxs-lookup"><span data-stu-id="982d3-351">Requirements</span></span>



| <span data-ttu-id="982d3-352">Требование</span><span class="sxs-lookup"><span data-stu-id="982d3-352">Requirement</span></span> | <span data-ttu-id="982d3-353">Значение</span><span class="sxs-lookup"><span data-stu-id="982d3-353">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="982d3-354">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="982d3-354">Minimum supported client</span></span><br/> | <span data-ttu-id="982d3-355">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="982d3-355">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="982d3-356">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="982d3-356">Minimum supported server</span></span><br/> | <span data-ttu-id="982d3-357">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="982d3-357">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="982d3-358">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="982d3-358">Namespace</span></span><br/>                | <span data-ttu-id="982d3-359">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="982d3-359">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="982d3-360">MOF</span><span class="sxs-lookup"><span data-stu-id="982d3-360">MOF</span></span><br/>                      | <dl> <span data-ttu-id="982d3-361"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-361"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="982d3-362">DLL</span><span class="sxs-lookup"><span data-stu-id="982d3-362">DLL</span></span><br/>                      | <dl> <span data-ttu-id="982d3-363"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="982d3-363"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="982d3-364">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="982d3-364">See also</span></span>

<dl> <dt>

[<span data-ttu-id="982d3-365">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="982d3-365">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




