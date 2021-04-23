---
description: Управление качеством видео
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: Управление качеством видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233ccd54cfcb98742abef9a91241e903c07ba549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991412"
---
# <a name="video-quality-management"></a><span data-ttu-id="fcd7c-103">Управление качеством видео</span><span class="sxs-lookup"><span data-stu-id="fcd7c-103">Video Quality Management</span></span>

<span data-ttu-id="fcd7c-104">В этом разделе описываются некоторые улучшения конвейера видео в Windows 7 для Microsoft Media Foundation и Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-104">This topic describes some improvements to the video pipeline in Windows 7, both for Microsoft Media Foundation and Microsoft DirectShow.</span></span>

<span data-ttu-id="fcd7c-105">В идеальном мире видео никогда не будет выгружаться, независимо от разрешения видео или загрузки ЦП или GPU.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-105">In a perfect world, video would never glitch, regardless of the video resolution or the CPU/GPU load.</span></span> <span data-ttu-id="fcd7c-106">Безусловно, в реальности конвейер видео должен иметь возможность работать с ограниченными аппаратными ресурсами, и он должен адаптивно адаптировать воспроизведение в среде системы.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-106">In reality, of course, the video pipeline must be able to cope with finite hardware resources, and it must adaptively tailor playback to the system environment.</span></span> <span data-ttu-id="fcd7c-107">Цели управления качеством видео:</span><span class="sxs-lookup"><span data-stu-id="fcd7c-107">The goals for video quality management are to:</span></span>

-   <span data-ttu-id="fcd7c-108">Уменьшение количества сбоев (пропущенных или последних кадров).</span><span class="sxs-lookup"><span data-stu-id="fcd7c-108">Reduce glitching (dropped or late frames).</span></span>
-   <span data-ttu-id="fcd7c-109">Сократите использование памяти, особенно в GPU.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-109">Reduce memory usage, especially in the GPU.</span></span>
-   <span data-ttu-id="fcd7c-110">Сократите энергопотребление, особенно на ноутбуках с питанием от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-110">Reduce power consumption, especially in laptops running on battery power.</span></span>
-   <span data-ttu-id="fcd7c-111">Получите лучшее качество изображения, учитывая ограничения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-111">Get the best image quality possible, given resource constraints.</span></span>
-   <span data-ttu-id="fcd7c-112">Синхронизация видео с аудио.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-112">Keep video synchronized with audio.</span></span>

<span data-ttu-id="fcd7c-113">Некоторые из этих целей не связаны, особенно в низкоуровневых системах.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-113">Some of these goals are contrary, particularly on low-end systems.</span></span> <span data-ttu-id="fcd7c-114">Как правило, существует компромисс между скоростью и качеством.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-114">Generally there is a trade-off between speed and quality.</span></span> <span data-ttu-id="fcd7c-115">Сбой является более нежелательным, чем умеренное уменьшение качества визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-115">Glitching is more objectionable than moderate reductions in visual quality.</span></span> <span data-ttu-id="fcd7c-116">Относительная важность потребления энергии зависит от среды. на ноутбуке, работающем на питании от аккумулятора, очень важно.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-116">The relative importance of power consumption varies with the environment; in a laptop running on battery power, it is very important.</span></span>

<span data-ttu-id="fcd7c-117">В Windows 7 Усовершенствованный модуль подготовки отчетов (Евр) обеспечивает улучшенную поддержку управления качеством видео.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-117">In Windows 7, the enhanced video renderer (EVR) has better support for video quality management.</span></span> <span data-ttu-id="fcd7c-118">Как конвейер Media Foundation, так и конвейер DirectShow были обновлены, чтобы воспользоваться преимуществами этих возможностей.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-118">Both the Media Foundation pipeline and the DirectShow pipeline have been updated to take advantage of these capabilities.</span></span> <span data-ttu-id="fcd7c-119">Используется существования такого двухаспектногой подход:</span><span class="sxs-lookup"><span data-stu-id="fcd7c-119">A two-pronged approach is used:</span></span>

-   <span data-ttu-id="fcd7c-120">Перед началом воспроизведения конвейер может выполнять статическую оптимизацию на основе параметров управления питанием пользователя и сведений об оборудовании.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-120">Before playback starts, the pipeline can perform static optimizations, based on the user's power management settings and information about the hardware.</span></span>
-   <span data-ttu-id="fcd7c-121">После начала воспроизведения конвейер может применять динамическую оптимизацию на основе производительности во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-121">After playback starts, the pipeline can apply dynamic optimizations, based on run-time performance.</span></span>

## <a name="quality-management-in-media-foundation"></a><span data-ttu-id="fcd7c-122">Управление качеством в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fcd7c-122">Quality Management in Media Foundation</span></span>

<span data-ttu-id="fcd7c-123">Чтобы включить статическую оптимизацию, перед разрешением топологии необходимо установить атрибут [ \_ статических средств \_ \_ \_ оптимизации воспроизведения топологии MF](mf-topology-static-playback-optimizations.md) в частичной топологии.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-123">To enable static optimizations, set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute on the partial topology before resolving the topology.</span></span> <span data-ttu-id="fcd7c-124">Загрузчик топологии запрашивает этот атрибут в методе [**имфтополоадер:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .</span><span class="sxs-lookup"><span data-stu-id="fcd7c-124">The topology loader queries this attribute in its [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="fcd7c-125">При включении статических оптимизаций необходимо задать два других атрибута в топологии:</span><span class="sxs-lookup"><span data-stu-id="fcd7c-125">If you enable static optimizations, you should set two other attributes on the topology:</span></span>



| <span data-ttu-id="fcd7c-126">attribute</span><span class="sxs-lookup"><span data-stu-id="fcd7c-126">Attribute</span></span>                                                                                                                                      | <span data-ttu-id="fcd7c-127">Описание</span><span class="sxs-lookup"><span data-stu-id="fcd7c-127">Description</span></span>                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fcd7c-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>\_ \_ Максимальное число воспроизведений для воспроизведения топологии MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="fcd7c-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span><br/>   | <span data-ttu-id="fcd7c-129">Указывает максимальный размер окна воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-129">Specifies the maximum size of the video playback window.</span></span><br/> |
| <span data-ttu-id="fcd7c-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>\_ \_ Частота воспроизведения в топологии MF \_</span><span class="sxs-lookup"><span data-stu-id="fcd7c-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span><br/> | <span data-ttu-id="fcd7c-131">Указывает частоту обновления монитора.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-131">Specifies the monitor refresh rate.</span></span><br/>                      |



 

<span data-ttu-id="fcd7c-132">Эти два атрибута помогают конвейеру рассчитать наиболее эффективный параметр для управления качеством.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-132">These two attributes help the pipeline calculate the most effective setting for quality management.</span></span>

<span data-ttu-id="fcd7c-133">Динамическая оптимизация выполняется диспетчером качества.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-133">Dynamic optimizations are performed by the quality manager.</span></span> <span data-ttu-id="fcd7c-134">Для включения диспетчера качества ничего делать не нужно. Он включается автоматически.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-134">You do not need to do anything to enable the quality manager; it is automatically enabled.</span></span> <span data-ttu-id="fcd7c-135">Диспетчер качества существовал в Windows Vista; в Windows 7 Евр может лучше реагировать на сообщения от диспетчера качества.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-135">The quality manager existed in Windows Vista; in Windows 7, the EVR can respond better to messages from the quality manager.</span></span>

## <a name="quality-management-in-directshow"></a><span data-ttu-id="fcd7c-136">Управление качеством в DirectShow</span><span class="sxs-lookup"><span data-stu-id="fcd7c-136">Quality Management in DirectShow</span></span>

<span data-ttu-id="fcd7c-137">DirectShow поддерживает статическую и динамическую оптимизацию для воспроизведения DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-137">DirectShow supports static and dynamic optimizations for DVD playback.</span></span> <span data-ttu-id="fcd7c-138">Чтобы включить эти оптимизации в приложении воспроизведения DVD, установите следующие флаги в параметре *dwFlags* метода **Идвдграфбуилдер:: рендердвдвидеоволуме** :</span><span class="sxs-lookup"><span data-stu-id="fcd7c-138">To enable these optimizations in a DVD playback application, set the following flags in the *dwFlags* parameter of the **IDvdGraphBuilder::RenderDvdVideoVolume** method:</span></span>



| <span data-ttu-id="fcd7c-139">Flag</span><span class="sxs-lookup"><span data-stu-id="fcd7c-139">Flag</span></span>                  | <span data-ttu-id="fcd7c-140">Описание</span><span class="sxs-lookup"><span data-stu-id="fcd7c-140">Description</span></span>                    |
|-----------------------|--------------------------------|
| <span data-ttu-id="fcd7c-141">\_Диаграмма на DVD-дисках \_ \_</span><span class="sxs-lookup"><span data-stu-id="fcd7c-141">AM\_DVD\_ADAPT\_GRAPH</span></span> | <span data-ttu-id="fcd7c-142">Включает статическую оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-142">Enables static optimizations.</span></span>  |
| <span data-ttu-id="fcd7c-143">\_ \_ Евр \_ качество обслуживания DVD</span><span class="sxs-lookup"><span data-stu-id="fcd7c-143">AM\_DVD\_EVR\_QOS</span></span>     | <span data-ttu-id="fcd7c-144">Включает динамическую оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-144">Enables dynamic optimizations.</span></span> |



 

<span data-ttu-id="fcd7c-145">Другие приложения DirectShow могут включить динамическую оптимизацию, вызвав метод [**иеврфилтерконфижекс:: сетконфигпрефс**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) непосредственно в фильтре Евр.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-145">Other DirectShow applications can enable dynamic optimizations by calling the [**IEVRFilterConfigEx::SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) method directly on the EVR filter.</span></span> <span data-ttu-id="fcd7c-146">Укажите флаг **еврфилтерконфигпрефс \_ енаблекос** .</span><span class="sxs-lookup"><span data-stu-id="fcd7c-146">Specify the **EVRFilterConfigPrefs\_EnableQoS** flag.</span></span>

> [!Note]  
> <span data-ttu-id="fcd7c-147">Статическая оптимизация в DirectShow ограничена воспроизведением DVD.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-147">Static optimizations in DirectShow are limited to DVD playback.</span></span>

 

## <a name="quality-management-in-the-evr"></a><span data-ttu-id="fcd7c-148">Управление качеством в Евр</span><span class="sxs-lookup"><span data-stu-id="fcd7c-148">Quality Management in the EVR</span></span>

<span data-ttu-id="fcd7c-149">Евр поддерживает некоторые новые флаги конфигурации для управления качеством.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-149">The EVR supports some new configuration flags for quality management.</span></span> <span data-ttu-id="fcd7c-150">Если включить оптимизацию управления качеством, описанную выше, не нужно задавать эти флаги напрямую.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-150">If you enable the quality management optimizations described previously, you do not have to set these flags directly.</span></span> <span data-ttu-id="fcd7c-151">Однако они задокументированы для приложений, которым требуется более детальный контроль над Евр.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-151">However, they are documented for applications that want more granular control over the EVR.</span></span>

<span data-ttu-id="fcd7c-152">Установите следующие флаги в микшере евр, вызвав метод [**IMFVideoMixerControl2:: сетмиксингпрефс**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) :</span><span class="sxs-lookup"><span data-stu-id="fcd7c-152">Set the following flags on the EVR mixer by calling the [**IMFVideoMixerControl2::SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fcd7c-153">Флаги</span><span class="sxs-lookup"><span data-stu-id="fcd7c-153">Flags</span></span></th>
<th><span data-ttu-id="fcd7c-154">Описание</span><span class="sxs-lookup"><span data-stu-id="fcd7c-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fcd7c-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="fcd7c-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span></span></li>
<li><span data-ttu-id="fcd7c-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="fcd7c-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="fcd7c-157">Пропустите второе поле каждого кадра с чередованием.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-157">Skip the second field of every interlaced frame.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fcd7c-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span><span class="sxs-lookup"><span data-stu-id="fcd7c-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span></span></li>
<li><span data-ttu-id="fcd7c-159"><strong>MFVideoMixPrefs_ForceBob</strong></span><span class="sxs-lookup"><span data-stu-id="fcd7c-159"><strong>MFVideoMixPrefs_ForceBob</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="fcd7c-160">Используйте несамостоятельную разчересстрочную развертку Боба, даже если драйвер поддерживает режим с чередованием более высокого качества.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-160">Use bob deinterlacing, even if the driver supports a higher-quality deinterlace mode.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fcd7c-161">Установите следующие флаги для выступающего евр, вызвав метод [**имфвидеодисплайконтрол:: сетрендерингпрефс**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) :</span><span class="sxs-lookup"><span data-stu-id="fcd7c-161">Set the following flags on the EVR presenter by calling the [**IMFVideoDisplayControl::SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fcd7c-162">Флаги</span><span class="sxs-lookup"><span data-stu-id="fcd7c-162">Flags</span></span></th>
<th><span data-ttu-id="fcd7c-163">Описание</span><span class="sxs-lookup"><span data-stu-id="fcd7c-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fcd7c-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="fcd7c-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span></span></li>
<li><span data-ttu-id="fcd7c-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="fcd7c-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="fcd7c-166">Регулирование выходных данных для соответствия пропускной способности GPU.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-166">Throttle output to match GPU bandwidth.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fcd7c-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span><span class="sxs-lookup"><span data-stu-id="fcd7c-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span></span></li>
<li><span data-ttu-id="fcd7c-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span><span class="sxs-lookup"><span data-stu-id="fcd7c-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="fcd7c-169">Вызовы пакетной службы Direct3D представлены в виде вызовов.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-169">Batch Direct3D Present calls.</span></span> <span data-ttu-id="fcd7c-170">Такая оптимизация позволяет системе переходить в состояние простоя чаще, что может снизить энергопотребление.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-170">This optimization enables the system to enter into idle states more frequently, which can reduce power consumption.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fcd7c-171">MFVideoRenderPrefs_ForceScaling</span><span class="sxs-lookup"><span data-stu-id="fcd7c-171">MFVideoRenderPrefs_ForceScaling</span></span></li>
<li><span data-ttu-id="fcd7c-172">MFVideoRenderPrefs_AllowScaling</span><span class="sxs-lookup"><span data-stu-id="fcd7c-172">MFVideoRenderPrefs_AllowScaling</span></span></li>
</ul></td>
<td><span data-ttu-id="fcd7c-173">Смешивание видео с помощью прямоугольника, размер которого меньше, чем прямоугольник вывода.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-173">Perform video mixing using a rectangle smaller than the output rectangle.</span></span> <span data-ttu-id="fcd7c-174">Масштабировать результат до правильного размера выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fcd7c-174">Scale the result to the correct output size.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fcd7c-175">Кроме того, приемник мультимедиа Евр поддерживает атрибуты конфигурации, соответствующие каждому из этих флагов:</span><span class="sxs-lookup"><span data-stu-id="fcd7c-175">In addition, the EVR media sink supports configuration attributes that correspond to each of these flags:</span></span>

-   [<span data-ttu-id="fcd7c-176">Еврконфиг \_ алловбатчинг</span><span class="sxs-lookup"><span data-stu-id="fcd7c-176">EVRConfig\_AllowBatching</span></span>](evrconfig-allowbatching.md)
-   [<span data-ttu-id="fcd7c-177">Еврконфиг \_ алловдроптобоб</span><span class="sxs-lookup"><span data-stu-id="fcd7c-177">EVRConfig\_AllowDropToBob</span></span>](evrconfig-allowdroptobob.md)
-   [<span data-ttu-id="fcd7c-178">Еврконфиг \_ алловдроптохалфинтерлаце</span><span class="sxs-lookup"><span data-stu-id="fcd7c-178">EVRConfig\_AllowDropToHalfInterlace</span></span>](evrconfig-allowdroptohalfinterlace.md)
-   [<span data-ttu-id="fcd7c-179">Еврконфиг \_ алловскалинг</span><span class="sxs-lookup"><span data-stu-id="fcd7c-179">EVRConfig\_AllowScaling</span></span>](evrconfig-allowscaling.md)
-   [<span data-ttu-id="fcd7c-180">Еврконфиг \_ алловдроптосроттле</span><span class="sxs-lookup"><span data-stu-id="fcd7c-180">EVRConfig\_AllowDropToThrottle</span></span>](evrconfig-allowdroptothrottle.md)
-   [<span data-ttu-id="fcd7c-181">Еврконфиг \_ форцебатчинг</span><span class="sxs-lookup"><span data-stu-id="fcd7c-181">EVRConfig\_ForceBatching</span></span>](evrconfig-forcebatching.md)
-   [<span data-ttu-id="fcd7c-182">Еврконфиг \_ форцебоб</span><span class="sxs-lookup"><span data-stu-id="fcd7c-182">EVRConfig\_ForceBob</span></span>](evrconfig-forcebob.md)
-   [<span data-ttu-id="fcd7c-183">Еврконфиг \_ форцехалфинтерлаце</span><span class="sxs-lookup"><span data-stu-id="fcd7c-183">EVRConfig\_ForceHalfInterlace</span></span>](evrconfig-forcehalfinterlace.md)
-   [<span data-ttu-id="fcd7c-184">Еврконфиг \_ форцескалинг</span><span class="sxs-lookup"><span data-stu-id="fcd7c-184">EVRConfig\_ForceScaling</span></span>](evrconfig-forcescaling.md)
-   [<span data-ttu-id="fcd7c-185">Еврконфиг \_ форцесроттле</span><span class="sxs-lookup"><span data-stu-id="fcd7c-185">EVRConfig\_ForceThrottle</span></span>](evrconfig-forcethrottle.md)

<span data-ttu-id="fcd7c-186">Перед началом воспроизведения эти атрибуты можно задать непосредственно в приемнике носителей Евр в качестве альтернативы вызову методов [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) и [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="fcd7c-186">Before playback starts, you can set these attributes directly on the EVR media sink, as an alternative to calling the [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) and [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) methods.</span></span> <span data-ttu-id="fcd7c-187">Чтобы задать эти атрибуты, выполните запрос к приемнику Евр мультимедиа для [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="fcd7c-187">To set these attributes, query the EVR media sink for [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcd7c-188">См. также</span><span class="sxs-lookup"><span data-stu-id="fcd7c-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcd7c-189">Сеанс мультимедиа</span><span class="sxs-lookup"><span data-stu-id="fcd7c-189">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 




