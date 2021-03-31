---
description: Режим смешения YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Режим смешения YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf4ca6b1ba5317145c410d6e5b899c7cf264f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912103"
---
# <a name="yuv-mixing-mode"></a><span data-ttu-id="5e183-103">Режим смешения YUV</span><span class="sxs-lookup"><span data-stu-id="5e183-103">YUV Mixing Mode</span></span>

<span data-ttu-id="5e183-104">Этот раздел относится к пакету обновления 2 (SP2) для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5e183-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="5e183-105">Начиная с пакета обновления 2 (SP2) для Windows XP, VMR поддерживает режим смешения, называемый режимом смешения YUV.</span><span class="sxs-lookup"><span data-stu-id="5e183-105">Starting in Windows XP Service Pack 2, the VMR supports a mixing mode called YUV mixing mode.</span></span> <span data-ttu-id="5e183-106">Этот режим лучше всего подходит для расширенных ТЕЛЕПЕРЕДАЧ или DVD-приложений.</span><span class="sxs-lookup"><span data-stu-id="5e183-106">This mode is most useful for advanced TV or DVD applications.</span></span> <span data-ttu-id="5e183-107">Она зарабатывает некоторые возможности микшера VMR для повышения производительности аппаратного оборудования, использующего архитектуру единой архитектуры памяти.</span><span class="sxs-lookup"><span data-stu-id="5e183-107">It trades some of the power of the VMR mixer for better performance on low end graphics hardware that uses a unified memory architecture design.</span></span> <span data-ttu-id="5e183-108">Режим смешения YUV поддерживается как для VMR-7, так и для VMR-9.</span><span class="sxs-lookup"><span data-stu-id="5e183-108">YUV mixing mode is supported on both the VMR-7 and VMR-9.</span></span>

<span data-ttu-id="5e183-109">**Преимущества**</span><span class="sxs-lookup"><span data-stu-id="5e183-109">**Advantages**</span></span>

<span data-ttu-id="5e183-110">Режим смешения YUV имеет несколько преимуществ, связанных с производительностью отрисовки в исходном режиме смешения RGB, поддерживаемом VMR:</span><span class="sxs-lookup"><span data-stu-id="5e183-110">YUV mixing mode has several advantages relating to rendering performance over the original RGB mixing mode supported by the VMR:</span></span>

-   <span data-ttu-id="5e183-111">Когда VMR находится в режиме смешения YUV, все операции композиции, выполняемые в процессе разчередования и воспроизведения видеопотоков, выполняются в пространстве цветов YUV.</span><span class="sxs-lookup"><span data-stu-id="5e183-111">When the VMR is in YUV mixing mode, all de-interlacing and video stream composition operations are performed in YUV color space.</span></span> <span data-ttu-id="5e183-112">Для поверхностей YUV обычно требуется от 50% до 60% меньше пропускной способности памяти, чем эквивалентные поверхности RGB.</span><span class="sxs-lookup"><span data-stu-id="5e183-112">YUV surfaces typically require from 50% to 60% less memory bandwidth than equivalent RGB surfaces.</span></span>
-   <span data-ttu-id="5e183-113">Разбиение и объединение потоков выполняется одним вызовом графического драйвера.</span><span class="sxs-lookup"><span data-stu-id="5e183-113">The deinterlacing and stream composition are performed by a single call to the graphics driver.</span></span> <span data-ttu-id="5e183-114">Драйвер может использовать возможности работы с несколькими текстурами графического оборудования, что приводит к дополнительной экономии пропускной способности памяти.</span><span class="sxs-lookup"><span data-stu-id="5e183-114">The driver can use the graphics hardware's multi-texturing capabilities, resulting in additional memory bandwidth savings.</span></span>

<span data-ttu-id="5e183-115">Хотя любое видеоприложение может использовать режим смешения YUV, оно в основном предназначено для двух типов приложений воспроизведения видео:</span><span class="sxs-lookup"><span data-stu-id="5e183-115">Although any video application can use YUV mixing mode, it is primarily intended for two types of video playback application:</span></span>

1.  <span data-ttu-id="5e183-116">ТВ-приложения, отображающие скрытые субтитры или телетекст.</span><span class="sxs-lookup"><span data-stu-id="5e183-116">TV applications that display closed captions or teletext.</span></span>
2.  <span data-ttu-id="5e183-117">В приложениях для DVD отображаются данные подизображения DVD или скрытые субтитры.</span><span class="sxs-lookup"><span data-stu-id="5e183-117">DVD applications display DVD subpicture data or closed captions.</span></span>

<span data-ttu-id="5e183-118">**Ограничения**</span><span class="sxs-lookup"><span data-stu-id="5e183-118">**Restrictions**</span></span>

<span data-ttu-id="5e183-119">При переводе в режим "Микширование YUV" для параметра VMR применяется ряд ограничений:</span><span class="sxs-lookup"><span data-stu-id="5e183-119">A number of restrictions are enforced by the VMR when it is put into YUV mixing mode:</span></span>

-   <span data-ttu-id="5e183-120">Поток 0 (поток, подключенный к входному контакту 0) может быть прогрессивным или чередованием; все остальные потоки должны быть прогрессивными.</span><span class="sxs-lookup"><span data-stu-id="5e183-120">Stream 0 (the stream connected to Input Pin 0) can be progressive or interlaced; all other streams must be progressive.</span></span>
-   <span data-ttu-id="5e183-121">Идентификатор GUID \_ null (режим "плетение") не допускается для потока 0.</span><span class="sxs-lookup"><span data-stu-id="5e183-121">GUID\_NULL (weave mode) is not allowed for stream 0.</span></span>
-   <span data-ttu-id="5e183-122">Деинтерлацепреф- \_ плетение нельзя использовать в качестве резервного режима, так как это может препятствовать созданию устройства без чередования.</span><span class="sxs-lookup"><span data-stu-id="5e183-122">DeinterlacePref\_Weave cannot be used as a fallback mode because this could prevent a de-interlace device from being created.</span></span> <span data-ttu-id="5e183-123">Режим смешения YUV требует чередования устройства, даже если входящее видео не чередуются.</span><span class="sxs-lookup"><span data-stu-id="5e183-123">YUV mixing mode requires a deinterlace device even if the incoming video is not interlaced.</span></span>
-   <span data-ttu-id="5e183-124">Нельзя вносить изменения в значение плоского альфа-канала, связанное с каждым входным потоком VMR.</span><span class="sxs-lookup"><span data-stu-id="5e183-124">No changes can be made to the planar alpha value associated with each VMR input stream.</span></span>
-   <span data-ttu-id="5e183-125">Пользователь не может изменить Z-порядок подключенных потоков видео.</span><span class="sxs-lookup"><span data-stu-id="5e183-125">The user cannot alter the Z-order of the connected video streams.</span></span> <span data-ttu-id="5e183-126">Z-порядок по умолчанию взят из порядка контактов.</span><span class="sxs-lookup"><span data-stu-id="5e183-126">The default Z-order is taken from the pin order.</span></span>
-   <span data-ttu-id="5e183-127">Ключ цвета не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5e183-127">Color keying is not supported.</span></span>
-   <span data-ttu-id="5e183-128">Входной ПИН-код 0 должен получить поток видео.</span><span class="sxs-lookup"><span data-stu-id="5e183-128">Input pin 0 must receive the video stream.</span></span>
-   <span data-ttu-id="5e183-129">Другие ПИН-коды ввода могут принимать только данные подпотока видео, такие как подизображение DVD, скрытые субтитры или телетекст.</span><span class="sxs-lookup"><span data-stu-id="5e183-129">The other inputs pins can only receive video sub-stream data such as DVD sub-picture, closed captions or teletext.</span></span>
-   <span data-ttu-id="5e183-130">Другие ПИН-коды ввода могут принимать только однопиксельные форматы YUV Alpha, такие как АЙУВ, AI44 и IA44.</span><span class="sxs-lookup"><span data-stu-id="5e183-130">The other inputs pins can only accept per-pixel alpha YUV formats, such as AYUV, AI44 and IA44.</span></span>
-   <span data-ttu-id="5e183-131">Ни один из входных ПИН-кодов VMR не может принимать какие-либо форматы RGB.</span><span class="sxs-lookup"><span data-stu-id="5e183-131">None of the VMR's input pins can accept any RGB formats.</span></span>
-   <span data-ttu-id="5e183-132">Указанные в приложении растровые изображения больше не могут быть объединены с видео до показа.</span><span class="sxs-lookup"><span data-stu-id="5e183-132">Application supplied bitmap images can no longer be combined with the video prior to presentation to the display.</span></span>
-   <span data-ttu-id="5e183-133">Отдельные подпотоки не могут быть инвертированы по горизонтали или по вертикали с помощью функций «выходного прямоугольника VMR».</span><span class="sxs-lookup"><span data-stu-id="5e183-133">Individual sub-streams cannot be inverted horizontally or vertically using the VMR's mixer "output rectangle" functions.</span></span> <span data-ttu-id="5e183-134">"Нормальное" перепозиционирование потоков и изменение размера поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5e183-134">"Normal" stream re-positioning and re-sizing is supported.</span></span>
-   <span data-ttu-id="5e183-135">Цвет фона смешивания (заданный параметром [**ивмрмиксерконтрол:: сетбаккграундклр**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) по-прежнему задается в цветовом пространстве RGB, точно так же, как в режиме смешения RGB.</span><span class="sxs-lookup"><span data-stu-id="5e183-135">The mixing background color (specified by [**IVMRMixerControl::SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) is still specified in the RGB color space, just as in RGB mixing mode.</span></span>

<span data-ttu-id="5e183-136">**Конфигурация**</span><span class="sxs-lookup"><span data-stu-id="5e183-136">**Configuration**</span></span>

<span data-ttu-id="5e183-137">Приложения должны явно настроить фильтр VMR, чтобы воспользоваться преимуществами режима смешения YUV. исходный режим смешения RGB остается в режиме смешения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e183-137">Applications must explicitly configure the VMR to take advantage of YUV mixing mode; the original RGB mixing mode remains the default mixing mode.</span></span> <span data-ttu-id="5e183-138">Чтобы включить режим смешения YUV в VMR-7, вызовите [**ивмрмиксерконтрол:: сетмиксингпрефс**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) с \_ флагом миксерпреф рендертаржетюв.</span><span class="sxs-lookup"><span data-stu-id="5e183-138">To enable YUV mixing mode in the VMR-7, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_RenderTargetYUV flag.</span></span> <span data-ttu-id="5e183-139">Этот вызов необходимо выполнить до подключения всех входных ПИН-кодов VMR.</span><span class="sxs-lookup"><span data-stu-id="5e183-139">This call must be made before any of the VMR's input pins are connected.</span></span> <span data-ttu-id="5e183-140">Чтобы включить режим смешения YUV в VMR-9, вызовите [**IVMRMixerControl9:: сетмиксингпрефс**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) с \_ флагом MixerPref9 рендертаржетюв.</span><span class="sxs-lookup"><span data-stu-id="5e183-140">To enable YUV mixing mode in the VMR-9, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_RenderTargetYUV flag.</span></span>

<span data-ttu-id="5e183-141">Единственный способ определить, поддерживает ли VMR-7 новый режим смешивания YUV, — это попробовать установить фильтр VMR в этом режиме.</span><span class="sxs-lookup"><span data-stu-id="5e183-141">The only way to determine if the VMR-7 supports the new YUV mixing mode is to try setting the VMR into that mode.</span></span> <span data-ttu-id="5e183-142">Если вызов будет выполнен, вы по-прежнему можете вернуть VMR в режим смешения RGB, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="5e183-142">If the call succeeds, you can still put the VMR back into RGB mixing mode if necessary.</span></span> <span data-ttu-id="5e183-143">После того как он переключается в режим смешения YUV, фильтр VMR может быть переведен в режим смешения RGB только после отключения всех входных контактов.</span><span class="sxs-lookup"><span data-stu-id="5e183-143">After it is set into YUV mixing mode, the VMR can only be changed back to RGB mixing mode after all input pins have been disconnected.</span></span>

<span data-ttu-id="5e183-144">В режиме смешения YUV можно уменьшить нагрузку на графический процессор (GPU), применив следующие флаги в методе **сетмиксингпрефс** :</span><span class="sxs-lookup"><span data-stu-id="5e183-144">In YUV mixing mode, you can reduce the load on the graphics processing unit (GPU) by applying the following flags in the **SetMixingPrefs** method:</span></span>



| <span data-ttu-id="5e183-145">Flag</span><span class="sxs-lookup"><span data-stu-id="5e183-145">Flag</span></span>                                                                                 | <span data-ttu-id="5e183-146">Описание</span><span class="sxs-lookup"><span data-stu-id="5e183-146">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="5e183-147">VMR-7: Миксерпреф \_ динамиксвитчтобобвмр-9: MixerPref9 \_ динамиксвитчтобоб</span><span class="sxs-lookup"><span data-stu-id="5e183-147">VMR-7: MixerPref\_DynamicSwitchToBOBVMR-9: MixerPref9\_DynamicSwitchToBOB</span></span><br/> | <span data-ttu-id="5e183-148">Переключитесь на разчересстрочную развертку Боба.</span><span class="sxs-lookup"><span data-stu-id="5e183-148">Switch to bob deinterlacing.</span></span>                                     |
| <span data-ttu-id="5e183-149">VMR-7: Миксерпреф \_ DynamicDecimateBy2VMR-9: миксерпреф \_ DynamicDecimateBy2</span><span class="sxs-lookup"><span data-stu-id="5e183-149">VMR-7: MixerPref\_DynamicDecimateBy2VMR-9: MixerPref\_DynamicDecimateBy2</span></span><br/>  | <span data-ttu-id="5e183-150">Децимации изображение с коэффициентом 2 по горизонтали и вертикали.</span><span class="sxs-lookup"><span data-stu-id="5e183-150">Decimate the image by a factor of 2 horizontally and vertically.</span></span> |



 

<span data-ttu-id="5e183-151">Эти флаги можно добавить или удалить во время работы графа фильтра. изменение применяется, когда микшер VMR формирует следующий кадр видео.</span><span class="sxs-lookup"><span data-stu-id="5e183-151">You can add or remove these flags while the filter graph is running; the change is applied when the VMR mixer composes the next video frame.</span></span> <span data-ttu-id="5e183-152">Флаги не являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="5e183-152">The flags are not mutually exclusive.</span></span> <span data-ttu-id="5e183-153">Эти параметры уменьшают качество изображения, поэтому обычно их следует применять только в том случае, если качество видео менее важно, например, если видео воспроизводится в небольшой части пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5e183-153">These settings reduce the quality of the image, so typically you would apply them only when video quality is less important — for example, if video is playing in a small portion of the user interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e183-154">См. также</span><span class="sxs-lookup"><span data-stu-id="5e183-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e183-155">Использование режима смешения VMR</span><span class="sxs-lookup"><span data-stu-id="5e183-155">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




