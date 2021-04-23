---
description: Чередование видео
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Чередование видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec10f49ef21f3701f85467a3f4a1c4b08d69df72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701793"
---
# <a name="video-interlacing"></a><span data-ttu-id="1f273-103">Чередование видео</span><span class="sxs-lookup"><span data-stu-id="1f273-103">Video Interlacing</span></span>

<span data-ttu-id="1f273-104">В этом разделе описывается, как источники и декодеры мультимедиа должны работать с чередованием видеоматериалов.</span><span class="sxs-lookup"><span data-stu-id="1f273-104">This topic describes how media sources and decoders should handle interlaced video content.</span></span>

<span data-ttu-id="1f273-105">Чтобы правильно декодировать и визуализировать видео с чередованием, необходимы следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="1f273-105">To decode and render interlaced video correctly, the following information is needed:</span></span>

-   <span data-ttu-id="1f273-106">Прогрессивная или чересстрочная развертка.</span><span class="sxs-lookup"><span data-stu-id="1f273-106">Progressive or interlaced.</span></span> <span data-ttu-id="1f273-107">Видеопоток может содержать прогрессивные кадры, чередующиеся кадры или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="1f273-107">A video stream can contain progressive frames, interlaced frames, or a mix of both.</span></span>

-   <span data-ttu-id="1f273-108">Поле превосходство.</span><span class="sxs-lookup"><span data-stu-id="1f273-108">Field dominance.</span></span> <span data-ttu-id="1f273-109">Поле превосходство описывает поле, отображаемое первым, верхнее поле или нижнее поле.</span><span class="sxs-lookup"><span data-stu-id="1f273-109">Field dominance describes which field appears first, the upper field or the lower field.</span></span>

-   <span data-ttu-id="1f273-110">Повторите первое поле.</span><span class="sxs-lookup"><span data-stu-id="1f273-110">Repeat first field.</span></span> <span data-ttu-id="1f273-111">Этот флаг используется в выпадающих до 3:2, если кадр является прогрессивным, но поток находится в режиме чередования.</span><span class="sxs-lookup"><span data-stu-id="1f273-111">This flag is used in 3:2 pulldown, when the frame is progressive but the stream is interlaced.</span></span> <span data-ttu-id="1f273-112">В этом контексте первое поле может быть полем верхнего или нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="1f273-112">In this context, the first field can be the upper or lower field.</span></span>

-   <span data-ttu-id="1f273-113">Поля с чередованием или одно поле.</span><span class="sxs-lookup"><span data-stu-id="1f273-113">Interleaved fields or single field.</span></span> <span data-ttu-id="1f273-114">Пример может содержать одно поле или два поля с чередованием.</span><span class="sxs-lookup"><span data-stu-id="1f273-114">A sample can hold either a single field, or two interleaved fields.</span></span> <span data-ttu-id="1f273-115">Если образец содержит одно поле, высота выборки составляет половину высоты рамки, так как этот пример содержит только половину строк сканирования для кадра.</span><span class="sxs-lookup"><span data-stu-id="1f273-115">If a sample contains a single field, the sample height is half the frame height, because the sample contains only half of the scan lines for a frame.</span></span> <span data-ttu-id="1f273-116">Рекомендуется использовать поля с чередованием, если только характеристики исходного содержимого не зависят от других характеристик.</span><span class="sxs-lookup"><span data-stu-id="1f273-116">Interleaved fields are recommended unless the characteristics of the source content dictate otherwise.</span></span>

<span data-ttu-id="1f273-117">Любая из этих характеристик может изменяться от одного образца к другому.</span><span class="sxs-lookup"><span data-stu-id="1f273-117">Any of these characteristics can change from one sample to the next.</span></span> <span data-ttu-id="1f273-118">Однако компоненты видео должны знать что-то о общем содержимом перед началом потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="1f273-118">However, video components need to know something about the overall content before streaming begins.</span></span> <span data-ttu-id="1f273-119">Например, если видео является чередованием, расширенному обработчику видео (Евр) требуется зарезервировать видеопамять для устранения неразрывной развертки.</span><span class="sxs-lookup"><span data-stu-id="1f273-119">For example, if the video is interlaced, the enhanced video renderer (EVR) needs to reserve video memory for the deinterlacing.</span></span> <span data-ttu-id="1f273-120">Если видео является полностью прогрессивным кадром, с другой стороны, ЕВР может оптимизировать конвейер отрисовки.</span><span class="sxs-lookup"><span data-stu-id="1f273-120">If the video is entirely progressive frames, on the other hand, the EVR can optimize the rendering pipeline.</span></span> <span data-ttu-id="1f273-121">Добавление шага дечередования в конвейер увеличивает задержку визуализации.</span><span class="sxs-lookup"><span data-stu-id="1f273-121">Adding a deinterlacing step to the pipeline increases the rendering latency.</span></span>

<span data-ttu-id="1f273-122">Сведения о чересстрочную развертке хранятся в двух местах:</span><span class="sxs-lookup"><span data-stu-id="1f273-122">Information about interlacing is stored in two places:</span></span>

-   <span data-ttu-id="1f273-123">Общие сведения о чересстрочную развертке в потоке помещаются в тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1f273-123">General information about the interlacing in a stream is placed in the media type.</span></span> <span data-ttu-id="1f273-124">Дополнительные сведения о типах носителей см. в разделе [типы носителей](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="1f273-124">For more information about media types, see [Media Types](media-types.md).</span></span>

-   <span data-ttu-id="1f273-125">Сведения, которые могут изменяться при каждом примере, помещаются в пример как атрибут.</span><span class="sxs-lookup"><span data-stu-id="1f273-125">Information that can change with each sample is placed on the sample as an attribute.</span></span> <span data-ttu-id="1f273-126">Дополнительные сведения о примерах см. в разделе [примеры носителей](media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="1f273-126">For more information about samples, see [Media Samples](media-samples.md).</span></span>

## <a name="interlace-information-in-the-media-type"></a><span data-ttu-id="1f273-127">Развертка информации в типе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1f273-127">Interlace Information in the Media Type</span></span>

<span data-ttu-id="1f273-128">Атрибут [**\_ \_ \_ режима чересстрочная развертки MF**](mf-mt-interlace-mode-attribute.md) для типа носителя описывает, как осуществляется чередование потока в целом.</span><span class="sxs-lookup"><span data-stu-id="1f273-128">The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute on the media type describes how the stream as a whole is interlaced.</span></span> <span data-ttu-id="1f273-129">Значение этого атрибута является членом перечисления [**мфвидеоинтерлацемоде**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) .</span><span class="sxs-lookup"><span data-stu-id="1f273-129">The value of this attribute is a member of the [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) enumeration.</span></span> <span data-ttu-id="1f273-130">Тип мультимедиа всегда должен иметь этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="1f273-130">A video media type should always have this attribute.</span></span>

-   <span data-ttu-id="1f273-131">Если поток содержит только прогрессивные кадры без чередующихся кадров, используйте Мфвидеоинтерлаце \_ прогрессивный.</span><span class="sxs-lookup"><span data-stu-id="1f273-131">If the stream contains only progressive frames, with no interlaced frames, use MFVideoInterlace\_Progressive.</span></span>
-   <span data-ttu-id="1f273-132">Если поток содержит только чередующиеся кадры, а каждый образец содержит два поля с чередованием, используйте Мфвидеоинтерлаце \_ фиелдинтерлеаведупперфирст или мфвидеоинтерлаце \_ фиелдинтерлеаведловерфирст.</span><span class="sxs-lookup"><span data-stu-id="1f273-132">If the stream contains only interlaced frames, and every sample contains two interleaved fields, use MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>
-   <span data-ttu-id="1f273-133">Если поток содержит только чередующиеся кадры, а каждый пример содержит одно поле, используйте Мфвидеоинтерлаце \_ фиелдсинглеуппер или мфвидеоинтерлаце \_ фиелдсинглеловер.</span><span class="sxs-lookup"><span data-stu-id="1f273-133">If the stream contains only interlaced frames, and every sample contains a single field, use MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span> <span data-ttu-id="1f273-134">Если поля переходят между верхним и нижним, то не имеет значения, какое из этих двух значений используется.</span><span class="sxs-lookup"><span data-stu-id="1f273-134">If the fields alternate between upper and lower, then it does not matter which of these two values is used.</span></span> <span data-ttu-id="1f273-135">Если формат содержит только верхние поля или просто более низкие поля, задайте значение, соответствующее содержимому.</span><span class="sxs-lookup"><span data-stu-id="1f273-135">If the format contains just upper fields, or just lower fields, then set the value that corresponds to the content.</span></span>
-   <span data-ttu-id="1f273-136">Если поток содержит сочетание чередующихся и последовательных кадров или если поле превосходство, задайте для типа носителя значение Мфвидеоинтерлаце \_ миксединтерлацеорпрогрессиве.</span><span class="sxs-lookup"><span data-stu-id="1f273-136">If the stream contains a mix of interlaced and progressive frames, or if the field dominance switches, set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span> <span data-ttu-id="1f273-137">Используйте примеры атрибутов для описания каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="1f273-137">Use sample attributes to describe each frame.</span></span>

<span data-ttu-id="1f273-138">В следующей таблице приведена сводка по этому атрибуту.</span><span class="sxs-lookup"><span data-stu-id="1f273-138">The following table summarizes this attribute.</span></span>



| <span data-ttu-id="1f273-139">\_ \_ режим чересстрочную РАЗВЕРТКи MF \_</span><span class="sxs-lookup"><span data-stu-id="1f273-139">MF\_MT\_INTERLACE\_MODE</span></span>                       | <span data-ttu-id="1f273-140">Чередующиеся?</span><span class="sxs-lookup"><span data-stu-id="1f273-140">Interlaced?</span></span> | <span data-ttu-id="1f273-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="1f273-141">Samples</span></span>                                  | <span data-ttu-id="1f273-142">Первое поле</span><span class="sxs-lookup"><span data-stu-id="1f273-142">First field</span></span>    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| <span data-ttu-id="1f273-143">Мфвидеоинтерлаце \_ прогрессивный</span><span class="sxs-lookup"><span data-stu-id="1f273-143">MFVideoInterlace\_Progressive</span></span>                 | <span data-ttu-id="1f273-144">Нет</span><span class="sxs-lookup"><span data-stu-id="1f273-144">No</span></span>          | <span data-ttu-id="1f273-145">Прогрессивная рамка</span><span class="sxs-lookup"><span data-stu-id="1f273-145">Progressive frame</span></span>                        | <span data-ttu-id="1f273-146">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1f273-146">Not applicable</span></span> |
| <span data-ttu-id="1f273-147">Мфвидеоинтерлаце \_ фиелдинтерлеаведупперфирст</span><span class="sxs-lookup"><span data-stu-id="1f273-147">MFVideoInterlace\_FieldInterleavedUpperFirst</span></span>  | <span data-ttu-id="1f273-148">Да</span><span class="sxs-lookup"><span data-stu-id="1f273-148">Yes</span></span>         | <span data-ttu-id="1f273-149">Поля с чередованием</span><span class="sxs-lookup"><span data-stu-id="1f273-149">Interleaved fields</span></span>                       | <span data-ttu-id="1f273-150">Верхняя первая</span><span class="sxs-lookup"><span data-stu-id="1f273-150">Upper first</span></span>    |
| <span data-ttu-id="1f273-151">Мфвидеоинтерлаце \_ фиелдинтерлеаведловерфирст</span><span class="sxs-lookup"><span data-stu-id="1f273-151">MFVideoInterlace\_FieldInterleavedLowerFirst</span></span>  | <span data-ttu-id="1f273-152">Да</span><span class="sxs-lookup"><span data-stu-id="1f273-152">Yes</span></span>         | <span data-ttu-id="1f273-153">Поля с чередованием</span><span class="sxs-lookup"><span data-stu-id="1f273-153">Interleaved fields</span></span>                       | <span data-ttu-id="1f273-154">Нижняя первая</span><span class="sxs-lookup"><span data-stu-id="1f273-154">Lower first</span></span>    |
| <span data-ttu-id="1f273-155">Мфвидеоинтерлаце \_ фиелдсинглеуппер</span><span class="sxs-lookup"><span data-stu-id="1f273-155">MFVideoInterlace\_FieldSingleUpper</span></span>            | <span data-ttu-id="1f273-156">Да</span><span class="sxs-lookup"><span data-stu-id="1f273-156">Yes</span></span>         | <span data-ttu-id="1f273-157">Одно поле</span><span class="sxs-lookup"><span data-stu-id="1f273-157">Single field</span></span>                             | <span data-ttu-id="1f273-158">Верхняя первая</span><span class="sxs-lookup"><span data-stu-id="1f273-158">Upper first</span></span>    |
| <span data-ttu-id="1f273-159">Мфвидеоинтерлаце \_ фиелдсинглеловер</span><span class="sxs-lookup"><span data-stu-id="1f273-159">MFVideoInterlace\_FieldSingleLower</span></span>            | <span data-ttu-id="1f273-160">Да</span><span class="sxs-lookup"><span data-stu-id="1f273-160">Yes</span></span>         | <span data-ttu-id="1f273-161">Одно поле</span><span class="sxs-lookup"><span data-stu-id="1f273-161">Single field</span></span>                             | <span data-ttu-id="1f273-162">Нижняя первая</span><span class="sxs-lookup"><span data-stu-id="1f273-162">Lower first</span></span>    |
| <span data-ttu-id="1f273-163">Мфвидеоинтерлаце \_ миксединтерлацеорпрогрессиве</span><span class="sxs-lookup"><span data-stu-id="1f273-163">MFVideoInterlace\_MixedInterlaceOrProgressive</span></span> | <span data-ttu-id="1f273-164">Может варьироваться</span><span class="sxs-lookup"><span data-stu-id="1f273-164">Can vary</span></span>    | <span data-ttu-id="1f273-165">Поля с чередованием или прогрессивные кадры</span><span class="sxs-lookup"><span data-stu-id="1f273-165">Interleaved fields or progressive frames</span></span> | <span data-ttu-id="1f273-166">Может варьироваться</span><span class="sxs-lookup"><span data-stu-id="1f273-166">Can vary</span></span>       |



 

<span data-ttu-id="1f273-167">Поля с чередованием и отдельные поля не могут быть смешанными.</span><span class="sxs-lookup"><span data-stu-id="1f273-167">Interleaved fields and single fields cannot be mixed.</span></span> <span data-ttu-id="1f273-168">Переключение с одного на другой требует изменения типа носителя.</span><span class="sxs-lookup"><span data-stu-id="1f273-168">Switching from one to another requires a media type change.</span></span>

## <a name="interlace-flags-on-samples"></a><span data-ttu-id="1f273-169">Чередование флагов для выборок</span><span class="sxs-lookup"><span data-stu-id="1f273-169">Interlace Flags on Samples</span></span>

<span data-ttu-id="1f273-170">Сведения, которые могут изменяться от одного образца к другому, указываются с помощью примеров атрибутов.</span><span class="sxs-lookup"><span data-stu-id="1f273-170">Information that can change from one sample to the next is indicated using sample attributes.</span></span> <span data-ttu-id="1f273-171">Чтобы получить или задать эти атрибуты, используйте интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="1f273-171">Use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to get or set these attributes.</span></span>

<span data-ttu-id="1f273-172">Все атрибуты чередования, перечисленные в этом разделе, имеют логические значения.</span><span class="sxs-lookup"><span data-stu-id="1f273-172">All of the interlacing attributes listed in this section have Boolean values.</span></span> <span data-ttu-id="1f273-173">Фактически каждый из этих атрибутов может иметь три значения: **true**, **false** или not set.</span><span class="sxs-lookup"><span data-stu-id="1f273-173">Effectively, each of these attributes can have three values: either **TRUE**, **FALSE**, or not set.</span></span> <span data-ttu-id="1f273-174">Если атрибут не задан, значение берется из типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1f273-174">If an attribute is not set, the value is taken from the media type.</span></span> <span data-ttu-id="1f273-175">Если задан атрибут, значение переопределяет тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1f273-175">If an attribute is set, the value overrides the media type.</span></span> <span data-ttu-id="1f273-176">Недопустимые сочетания флагов и типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1f273-176">Some combinations of flags and media types are not valid.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f273-177">attribute</span><span class="sxs-lookup"><span data-stu-id="1f273-177">Attribute</span></span></th>
<th><span data-ttu-id="1f273-178">Описание</span><span class="sxs-lookup"><span data-stu-id="1f273-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f273-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span><span class="sxs-lookup"><span data-stu-id="1f273-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span></span></td>
<td><span data-ttu-id="1f273-180"><strong>Значение true</strong>показывает, что кадр является чередованием.</span><span class="sxs-lookup"><span data-stu-id="1f273-180">If <strong>TRUE</strong>, the frame is interlaced.</span></span> <span data-ttu-id="1f273-181">Если <strong>значение равно false</strong>, кадр является прогрессивным.</span><span class="sxs-lookup"><span data-stu-id="1f273-181">If <strong>FALSE</strong>, the frame is progressive.</span></span><br/> <span data-ttu-id="1f273-182">Установите этот атрибут для каждого образца, если тип носителя — MFVideoInterlace_MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="1f273-182">Set this attribute on every sample if the media type is MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f273-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span><span class="sxs-lookup"><span data-stu-id="1f273-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span></span></td>
<td><span data-ttu-id="1f273-184">Значение этого флага зависит от того, содержат ли образцы поля с чередованием или отдельные поля.</span><span class="sxs-lookup"><span data-stu-id="1f273-184">The meaning of this flag depends on whether the samples contain interleaved fields or single fields.</span></span><br/>
<ul>
<li><span data-ttu-id="1f273-185">Поля с чередованием: Если <strong>значение равно true</strong>, то нижнее поле является первым.</span><span class="sxs-lookup"><span data-stu-id="1f273-185">Interleaved fields: If <strong>TRUE</strong>, the lower field is first.</span></span> <span data-ttu-id="1f273-186">Если <strong>значение равно false</strong>, то верхнее поле является первым.</span><span class="sxs-lookup"><span data-stu-id="1f273-186">If <strong>FALSE</strong>, the upper field is first.</span></span><br/></li>
<li><span data-ttu-id="1f273-187">Одиночные поля: Если <strong>значение true</strong>, образец содержит меньшее поле.</span><span class="sxs-lookup"><span data-stu-id="1f273-187">Single fields: If <strong>TRUE</strong>, the sample contains a lower field.</span></span> <span data-ttu-id="1f273-188">Если <strong>значение равно false</strong>, образец содержит верхнее поле.</span><span class="sxs-lookup"><span data-stu-id="1f273-188">If <strong>FALSE</strong>, the sample contains an upper field.</span></span><br/></li>
</ul>
<span data-ttu-id="1f273-189">Установите этот атрибут для каждого образца развертки, если тип носителя — MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower или MFVideoInterlace_MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="1f273-189">Set this attribute on every interlace sample if the media type is MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower, or MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f273-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span><span class="sxs-lookup"><span data-stu-id="1f273-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span></span></td>
<td><span data-ttu-id="1f273-191">Если <strong>значение равно true</strong>, первое поле повторяется.</span><span class="sxs-lookup"><span data-stu-id="1f273-191">If <strong>TRUE</strong>, the first field is repeated.</span></span> <span data-ttu-id="1f273-192">Если значение равно <strong>false</strong> или не задано, первое поле не повторяется.</span><span class="sxs-lookup"><span data-stu-id="1f273-192">If <strong>FALSE</strong> or not set, the first field is not repeated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f273-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span><span class="sxs-lookup"><span data-stu-id="1f273-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span></span></td>
<td><span data-ttu-id="1f273-194">Если <strong>значение — true</strong>, пример содержит одно поле.</span><span class="sxs-lookup"><span data-stu-id="1f273-194">If <strong>TRUE</strong>, the sample contains a single field.</span></span> <span data-ttu-id="1f273-195">Если <strong>значение равно false</strong>, пример содержит поля с чередованием.</span><span class="sxs-lookup"><span data-stu-id="1f273-195">If <strong>FALSE</strong>, the sample contains interleaved fields.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1f273-196">В следующей таблице показано, какие флаги являются обязательными, необязательными или запрещенными в зависимости от типа носителя.</span><span class="sxs-lookup"><span data-stu-id="1f273-196">The following table shows which flags are required, optional, or prohibited, based on the media type.</span></span>



| <span data-ttu-id="1f273-197">Тип носителя</span><span class="sxs-lookup"><span data-stu-id="1f273-197">Media Type</span></span>         | <span data-ttu-id="1f273-198">Флаг чередования</span><span class="sxs-lookup"><span data-stu-id="1f273-198">Interlaced Flag</span></span>                      | <span data-ttu-id="1f273-199">Флаг Боттомфиелдфирст</span><span class="sxs-lookup"><span data-stu-id="1f273-199">BottomFieldFirst Flag</span></span>                    | <span data-ttu-id="1f273-200">Флаг Репеатфирстфиелд</span><span class="sxs-lookup"><span data-stu-id="1f273-200">RepeatFirstField Flag</span></span> | <span data-ttu-id="1f273-201">Флаг Синглефиелд</span><span class="sxs-lookup"><span data-stu-id="1f273-201">SingleField Flag</span></span>                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| <span data-ttu-id="1f273-202">прогрессивный</span><span class="sxs-lookup"><span data-stu-id="1f273-202">Progressive</span></span>        | <span data-ttu-id="1f273-203">Используемых Если задано, аргумент должен иметь **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1f273-203">Optional; if set, must be **FALSE**.</span></span> | <span data-ttu-id="1f273-204">Не задавайте.</span><span class="sxs-lookup"><span data-stu-id="1f273-204">Do not set.</span></span>                              | <span data-ttu-id="1f273-205">Не задавайте.</span><span class="sxs-lookup"><span data-stu-id="1f273-205">Do not set.</span></span>           | <span data-ttu-id="1f273-206">Не задавайте.</span><span class="sxs-lookup"><span data-stu-id="1f273-206">Do not set.</span></span>                          |
| <span data-ttu-id="1f273-207">Поля с чередованием</span><span class="sxs-lookup"><span data-stu-id="1f273-207">Interleaved fields</span></span> | <span data-ttu-id="1f273-208">Используемых Если задано, то параметр должен иметь **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1f273-208">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="1f273-209">Используемых Если параметр задан, должен соответствовать тип носителя.</span><span class="sxs-lookup"><span data-stu-id="1f273-209">Optional; if set, must match media type.</span></span> | <span data-ttu-id="1f273-210">Не задавайте.</span><span class="sxs-lookup"><span data-stu-id="1f273-210">Do not set.</span></span>           | <span data-ttu-id="1f273-211">Используемых Если задано, аргумент должен иметь **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1f273-211">Optional; if set, must be **FALSE**.</span></span> |
| <span data-ttu-id="1f273-212">Отдельные поля</span><span class="sxs-lookup"><span data-stu-id="1f273-212">Single fields</span></span>      | <span data-ttu-id="1f273-213">Используемых Если задано, то параметр должен иметь **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1f273-213">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="1f273-214">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="1f273-214">Required.</span></span>                                | <span data-ttu-id="1f273-215">Не задавайте.</span><span class="sxs-lookup"><span data-stu-id="1f273-215">Do not set.</span></span>           | <span data-ttu-id="1f273-216">Задайте значение **true**.</span><span class="sxs-lookup"><span data-stu-id="1f273-216">Set to **TRUE**.</span></span>                     |
| <span data-ttu-id="1f273-217">Смешанный</span><span class="sxs-lookup"><span data-stu-id="1f273-217">Mixed</span></span>              | <span data-ttu-id="1f273-218">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="1f273-218">Required.</span></span>                            | <span data-ttu-id="1f273-219">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="1f273-219">Required.</span></span>                                | <span data-ttu-id="1f273-220">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="1f273-220">Required.</span></span>             | <span data-ttu-id="1f273-221">Используемых Если задано, аргумент должен иметь **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1f273-221">Optional; if set, must be **FALSE**.</span></span> |



 

<span data-ttu-id="1f273-222">В случаях, когда атрибут является необязательным, тип мультимедиа уже определяет информацию.</span><span class="sxs-lookup"><span data-stu-id="1f273-222">In the cases where the attribute is optional, the media type already defines the information.</span></span> <span data-ttu-id="1f273-223">Допускается установить для атрибута значение match, но не обязательно.</span><span class="sxs-lookup"><span data-stu-id="1f273-223">It is valid to set the attribute to match, but not required.</span></span>

<span data-ttu-id="1f273-224">Например, если тип носителя — Мфвидеоинтерлаце \_ прогрессивно, это означает, что все кадры в потоке прогрессивны.</span><span class="sxs-lookup"><span data-stu-id="1f273-224">For example, if the media type is MFVideoInterlace\_Progressive, it implies that all frames in the stream are progressive.</span></span> <span data-ttu-id="1f273-225">Таким образом, можно задать для атрибута **мфсампликстенсион \_ чередование** **значение false** или оставить атрибут неопределенным.</span><span class="sxs-lookup"><span data-stu-id="1f273-225">Therefore, you can either set the **MFSampleExtension\_Interlaced** attribute to **FALSE**, or leave the attribute unset.</span></span>

## <a name="recommendations"></a><span data-ttu-id="1f273-226">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="1f273-226">Recommendations</span></span>

<span data-ttu-id="1f273-227">Этот раздел содержит рекомендации по различным типам содержимого.</span><span class="sxs-lookup"><span data-stu-id="1f273-227">This section contains recommendations for various types of content.</span></span>

1. <span data-ttu-id="1f273-228">Видео — это все прогрессивные кадры.</span><span class="sxs-lookup"><span data-stu-id="1f273-228">The video is all progressive frames.</span></span>

-   <span data-ttu-id="1f273-229">Задайте для типа носителя Мфвидеоинтерлаце \_ прогрессивный.</span><span class="sxs-lookup"><span data-stu-id="1f273-229">Set the media type to MFVideoInterlace\_Progressive.</span></span>

-   <span data-ttu-id="1f273-230">Не устанавливайте атрибут **мфсампликстенсион \_ чересстрочная развертки** или задайте для него **значение false** в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="1f273-230">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="1f273-231">Не устанавливайте атрибуты **мфсампликстенсион \_ боттомфиелдфирст**, **мфсампликстенсион \_ репеатфирстфиелд** или **мфсампликстенсион \_ SingleField** .</span><span class="sxs-lookup"><span data-stu-id="1f273-231">Do not set the **MFSampleExtension\_BottomFieldFirst**, **MFSampleExtension\_RepeatFirstField**, or **MFSampleExtension\_SingleField** attributes.</span></span>

2. <span data-ttu-id="1f273-232">Видео — это все поля с чередованием с одним и тем же полем превосходство.</span><span class="sxs-lookup"><span data-stu-id="1f273-232">The video is all interlaced fields with the same field dominance.</span></span> <span data-ttu-id="1f273-233">Примеры содержат поля с чередованием.</span><span class="sxs-lookup"><span data-stu-id="1f273-233">Samples contain interleaved fields.</span></span>

-   <span data-ttu-id="1f273-234">Задайте тип носителя Мфвидеоинтерлаце \_ фиелдинтерлеаведупперфирст или мфвидеоинтерлаце \_ фиелдинтерлеаведловерфирст.</span><span class="sxs-lookup"><span data-stu-id="1f273-234">Set the media type to MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>

-   <span data-ttu-id="1f273-235">Не устанавливайте атрибут **мфсампликстенсион \_ чересстрочная развертки** или задайте для него **значение true** в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="1f273-235">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="1f273-236">Не устанавливайте атрибут **мфсампликстенсион \_ боттомфиелдфирст** или задайте значение для каждого кадра в соответствии с типом носителя.</span><span class="sxs-lookup"><span data-stu-id="1f273-236">Do not set the **MFSampleExtension\_BottomFieldFirst** attribute, or set the value on every frame to match the media type.</span></span>

-   <span data-ttu-id="1f273-237">Не устанавливайте атрибут **мфсампликстенсион \_ репеатфирстфиелд** или задайте для него **значение false** в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="1f273-237">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="1f273-238">Не устанавливайте атрибут **мфсампликстенсион \_ синглефиелд** или задайте для него **значение false** в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="1f273-238">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

3. <span data-ttu-id="1f273-239">Видео содержит сочетание чередующихся и последовательных кадров с повторяющимися полями и различным полем превосходство (например, DVD Video).</span><span class="sxs-lookup"><span data-stu-id="1f273-239">The video contains a mix of interlaced and progressive frames, with repeated fields and varying field dominance (for example, DVD video).</span></span>

-   <span data-ttu-id="1f273-240">Задайте для типа носителя значение Мфвидеоинтерлаце \_ миксединтерлацеорпрогрессиве.</span><span class="sxs-lookup"><span data-stu-id="1f273-240">Set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span>

-   <span data-ttu-id="1f273-241">На каждом кадре задайте атрибуты **мфсампликстенсион \_ чередования**, **мфсампликстенсион \_ боттомфиелдфирст** и **мфсампликстенсион \_ репеатфирстфиелд** .</span><span class="sxs-lookup"><span data-stu-id="1f273-241">On every frame, set the **MFSampleExtension\_Interlaced**, **MFSampleExtension\_BottomFieldFirst**, and **MFSampleExtension\_RepeatFirstField** attributes.</span></span>

-   <span data-ttu-id="1f273-242">Не устанавливайте атрибут **мфсампликстенсион \_ синглефиелд** или задайте для него **значение false** в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="1f273-242">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

4. <span data-ttu-id="1f273-243">Видео чередуются, а примеры содержат отдельные поля.</span><span class="sxs-lookup"><span data-stu-id="1f273-243">The video is interlaced and samples contain single fields.</span></span>

-   <span data-ttu-id="1f273-244">Задайте тип носителя Мфвидеоинтерлаце \_ фиелдсинглеуппер или мфвидеоинтерлаце \_ фиелдсинглеловер.</span><span class="sxs-lookup"><span data-stu-id="1f273-244">Set the media type to MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span>

-   <span data-ttu-id="1f273-245">На каждом кадре задайте атрибут **мфсампликстенсион \_ боттомфиелдфирст** .</span><span class="sxs-lookup"><span data-stu-id="1f273-245">On every frame, set the **MFSampleExtension\_BottomFieldFirst** attribute.</span></span>

-   <span data-ttu-id="1f273-246">Не устанавливайте атрибут **мфсампликстенсион \_ чересстрочная развертки** или задайте для него **значение true** в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="1f273-246">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="1f273-247">Не устанавливайте атрибут **мфсампликстенсион \_ репеатфирстфиелд** или задайте для него **значение false** в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="1f273-247">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="1f273-248">Не устанавливайте атрибут **мфсампликстенсион \_ синглефиелд** или задайте для него **значение true** в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="1f273-248">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **TRUE** on every frame.</span></span>

<span data-ttu-id="1f273-249">Большинство видеоматериалов попадает в одну из этих категорий.</span><span class="sxs-lookup"><span data-stu-id="1f273-249">Most video content falls into one of these categories.</span></span>

## <a name="mpeg-2-mappings"></a><span data-ttu-id="1f273-250">Сопоставления MPEG-2</span><span class="sxs-lookup"><span data-stu-id="1f273-250">MPEG-2 Mappings</span></span>

<span data-ttu-id="1f273-251">Для содержимого MPEG-2 Используйте следующие сопоставления для преобразования флагов MPEG-2 в Media Foundation образцы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="1f273-251">For MPEG-2 content, use the following mappings to convert the MPEG-2 flags to Media Foundation sample attributes.</span></span>

<span data-ttu-id="1f273-252">**\_Структура рисунка**</span><span class="sxs-lookup"><span data-stu-id="1f273-252">**picture\_structure**</span></span>



| <span data-ttu-id="1f273-253">Значение</span><span class="sxs-lookup"><span data-stu-id="1f273-253">Value</span></span>         | <span data-ttu-id="1f273-254">Пример атрибута</span><span class="sxs-lookup"><span data-stu-id="1f273-254">Sample Attribute</span></span>                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f273-255">frame</span><span class="sxs-lookup"><span data-stu-id="1f273-255">frame</span></span>         | <span data-ttu-id="1f273-256">**Мфсампликстенсион \_ Синглефиелд**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="1f273-256">**MFSampleExtension\_SingleField** = **FALSE**</span></span>                                                                          |
| <span data-ttu-id="1f273-257">верхнее \_ поле</span><span class="sxs-lookup"><span data-stu-id="1f273-257">top\_field</span></span>    | <span data-ttu-id="1f273-258">**Мфсампликстенсион \_ Синглефиелд**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="1f273-258">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="1f273-259">**Мфсампликстенсион \_ Боттомфиелдфирст**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="1f273-259">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span><br/> |
| <span data-ttu-id="1f273-260">нижнее \_ поле</span><span class="sxs-lookup"><span data-stu-id="1f273-260">bottom\_field</span></span> | <span data-ttu-id="1f273-261">**Мфсампликстенсион \_ Синглефиелд**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="1f273-261">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="1f273-262">**Мфсампликстенсион \_ Боттомфиелдфирст**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="1f273-262">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span><br/>  |



 

<span data-ttu-id="1f273-263">**Прогрессивная \_ рамка**</span><span class="sxs-lookup"><span data-stu-id="1f273-263">**progressive\_frame**</span></span>



| <span data-ttu-id="1f273-264">Значение</span><span class="sxs-lookup"><span data-stu-id="1f273-264">Value</span></span> | <span data-ttu-id="1f273-265">Пример атрибута</span><span class="sxs-lookup"><span data-stu-id="1f273-265">Sample Attribute</span></span>                              |
|-------|-----------------------------------------------|
| <span data-ttu-id="1f273-266">0</span><span class="sxs-lookup"><span data-stu-id="1f273-266">0</span></span>     | <span data-ttu-id="1f273-267">**Мфсампликстенсион \_ С чередованием**,  =  **Истина**</span><span class="sxs-lookup"><span data-stu-id="1f273-267">**MFSampleExtension\_Interlaced** = **TRUE**</span></span>  |
| <span data-ttu-id="1f273-268">1</span><span class="sxs-lookup"><span data-stu-id="1f273-268">1</span></span>     | <span data-ttu-id="1f273-269">**Мфсампликстенсион \_ С чередованием**  =  </span><span class="sxs-lookup"><span data-stu-id="1f273-269">**MFSampleExtension\_Interlaced** = **FALSE**</span></span> |



 

<span data-ttu-id="1f273-270">**Сначала верхнее \_ поле \_**</span><span class="sxs-lookup"><span data-stu-id="1f273-270">**top\_field\_first**</span></span>



| <span data-ttu-id="1f273-271">Значение</span><span class="sxs-lookup"><span data-stu-id="1f273-271">Value</span></span> | <span data-ttu-id="1f273-272">Пример атрибута</span><span class="sxs-lookup"><span data-stu-id="1f273-272">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="1f273-273">0</span><span class="sxs-lookup"><span data-stu-id="1f273-273">0</span></span>     | <span data-ttu-id="1f273-274">**Мфсампликстенсион \_ Боттомфиелдфирст**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="1f273-274">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span>  |
| <span data-ttu-id="1f273-275">1</span><span class="sxs-lookup"><span data-stu-id="1f273-275">1</span></span>     | <span data-ttu-id="1f273-276">**Мфсампликстенсион \_ Боттомфиелдфирст**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="1f273-276">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span> |



 

<span data-ttu-id="1f273-277">**повторить \_ первое \_ поле**</span><span class="sxs-lookup"><span data-stu-id="1f273-277">**repeat\_first\_field**</span></span>



| <span data-ttu-id="1f273-278">Значение</span><span class="sxs-lookup"><span data-stu-id="1f273-278">Value</span></span> | <span data-ttu-id="1f273-279">Пример атрибута</span><span class="sxs-lookup"><span data-stu-id="1f273-279">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="1f273-280">0</span><span class="sxs-lookup"><span data-stu-id="1f273-280">0</span></span>     | <span data-ttu-id="1f273-281">**Мфсампликстенсион \_ Репеатфирстфиелд**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="1f273-281">**MFSampleExtension\_RepeatFirstField** = **FALSE**</span></span> |
| <span data-ttu-id="1f273-282">1</span><span class="sxs-lookup"><span data-stu-id="1f273-282">1</span></span>     | <span data-ttu-id="1f273-283">**Мфсампликстенсион \_ Репеатфирстфиелд**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="1f273-283">**MFSampleExtension\_RepeatFirstField** = **TRUE**</span></span>  |



 

## <a name="single-field-samples"></a><span data-ttu-id="1f273-284">Примеры Single-Field</span><span class="sxs-lookup"><span data-stu-id="1f273-284">Single-Field Samples</span></span>

<span data-ttu-id="1f273-285">Если тип носителя — Мфвидеоинтерлаце \_ фиелдсинглеуппер или мфвидеоинтерлаце \_ фиелдсинглеловер, это означает, что каждый пример содержит одно поле.</span><span class="sxs-lookup"><span data-stu-id="1f273-285">If the media type is MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower, it means that each sample contains a single field.</span></span> <span data-ttu-id="1f273-286">Однако тип носителя описывает весь кадр.</span><span class="sxs-lookup"><span data-stu-id="1f273-286">However, the media type describes the entire frame.</span></span> <span data-ttu-id="1f273-287">Таким образом, каждый буфер содержит только половину числа строк полей, указанных в типе носителя.</span><span class="sxs-lookup"><span data-stu-id="1f273-287">Therefore, each buffer contains only half the number of field lines given in the media type.</span></span> <span data-ttu-id="1f273-288">Например, если тип носителя описывает видео как 720 × 480, каждое поле содержит 240 строк сканирования, поэтому каждый буфер содержит только 240 строки пикселей.</span><span class="sxs-lookup"><span data-stu-id="1f273-288">For example, if the media type describes the video as 720 × 480, each field contains 240 scan lines, and therefore each buffer contains only 240 rows of pixels.</span></span> <span data-ttu-id="1f273-289">При написании компонента, который принимает типы мультимедиа с образцами с одним полем, этот факт следует принять во внимание при доступе к данным в буфере.</span><span class="sxs-lookup"><span data-stu-id="1f273-289">If you write a component that accepts media types with single-field samples, you must take this fact into account when you access the data in the buffer.</span></span>

<span data-ttu-id="1f273-290">То же правило применяется к геометрической апертуре (атрибуту «[ \_ \_ \_ Апертура по геометру](mf-mt-geometric-aperture-attribute.md) ») и по минимальному отображаемому апертуру (атрибуту[ \_ \_ \_ \_ апертуры MF-монитора](mf-mt-minimum-display-aperture-attribute.md) ).</span><span class="sxs-lookup"><span data-stu-id="1f273-290">The same rule applies to the geometric aperture ([MF\_MT\_GEOMETRIC\_APERTURE](mf-mt-geometric-aperture-attribute.md) attribute) and minimum display aperture ([MF\_MT\_MINIMUM\_DISPLAY\_APERTURE](mf-mt-minimum-display-aperture-attribute.md) attribute).</span></span> <span data-ttu-id="1f273-291">Эти регионы задаются в терминах всего кадра, а не отдельных полей.</span><span class="sxs-lookup"><span data-stu-id="1f273-291">These regions are specified in terms of the entire frame, not the individual fields.</span></span>

## <a name="directshow-mappings"></a><span data-ttu-id="1f273-292">Сопоставления DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f273-292">DirectShow Mappings</span></span>

<span data-ttu-id="1f273-293">В DirectShow сведения о чересстрочную развертке для отдельных примеров содержатся в элементе **двтипеспеЦификфлагс** структуры **\_ \_ свойств SAMPLE2** .</span><span class="sxs-lookup"><span data-stu-id="1f273-293">In DirectShow, per-sample interlacing information is contained in the **dwTypeSpecificFlags** member of the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="1f273-294">В следующей таблице показаны эквивалентные атрибуты для Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1f273-294">The following table shows the equivalent attributes for Media Foundation.</span></span>



| <span data-ttu-id="1f273-295">Флаг образца DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f273-295">DirectShow sample flag</span></span>              | <span data-ttu-id="1f273-296">Пример атрибута Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f273-296">Media Foundation sample attribute</span></span>                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f273-297">видеофлаг AM — \_ \_ \_ кадр с чередованием \_</span><span class="sxs-lookup"><span data-stu-id="1f273-297">AM\_VIDEO\_FLAG\_INTERLEAVED\_FRAME</span></span> | <span data-ttu-id="1f273-298">**Мфсампликстенсион \_ Синглефиелд**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="1f273-298">**MFSampleExtension\_SingleField** = **FALSE**.</span></span>                                                                                                                                    |
| <span data-ttu-id="1f273-299">\_Флаг видео \_ \_ FIELD1</span><span class="sxs-lookup"><span data-stu-id="1f273-299">AM\_VIDEO\_FLAG\_FIELD1</span></span>             | <span data-ttu-id="1f273-300">**Мфсампликстенсион \_ С чередованием**  =  .</span><span class="sxs-lookup"><span data-stu-id="1f273-300">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="1f273-301">**Мфсампликстенсион \_ Синглефиелд**  =  **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1f273-301">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="1f273-302">**Мфсампликстенсион \_ Боттомфиелдфирст**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="1f273-302">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span><br/> |
| <span data-ttu-id="1f273-303">\_FIELD2, \_ флажок AM Video \_</span><span class="sxs-lookup"><span data-stu-id="1f273-303">AM\_VIDEO\_FLAG\_FIELD2</span></span>             | <span data-ttu-id="1f273-304">**Мфсампликстенсион \_ С чередованием**  =  .</span><span class="sxs-lookup"><span data-stu-id="1f273-304">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="1f273-305">**Мфсампликстенсион \_ Синглефиелд**  =  **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1f273-305">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="1f273-306">**Мфсампликстенсион \_ Боттомфиелдфирст**  =  **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1f273-306">**MFSampleExtension\_BottomFieldFirst** = **TRUE**.</span></span><br/>  |
| <span data-ttu-id="1f273-307">\_ \_ наплетение флага видео \_</span><span class="sxs-lookup"><span data-stu-id="1f273-307">AM\_VIDEO\_FLAG\_WEAVE</span></span>              | <span data-ttu-id="1f273-308">**Мфсампликстенсион \_ С чередованием**  =  **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1f273-308">**MFSampleExtension\_Interlaced** = **FALSE**.</span></span> <span data-ttu-id="1f273-309">(Этот флаг указывает, что драйвер не должен размечать два поля.)</span><span class="sxs-lookup"><span data-stu-id="1f273-309">(This flag indicates that the driver should not deinterlace the two fields.)</span></span>                                                        |
| <span data-ttu-id="1f273-310">\_FIELD1FIRST, \_ флажок AM Video \_</span><span class="sxs-lookup"><span data-stu-id="1f273-310">AM\_VIDEO\_FLAG\_FIELD1FIRST</span></span>        | <span data-ttu-id="1f273-311">**Мфсампликстенсион \_ Боттомфиелдфирст**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="1f273-311">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> <span data-ttu-id="1f273-312">Если содержимое с чередованием и \_ \_ \_ флаг FIELD1FIRST не установлен, установите для этого атрибута **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1f273-312">If the content is interlaced and the AM\_VIDEO\_FLAG\_FIELD1FIRST flag is not present, set this attribute to **TRUE**.</span></span>        |
| <span data-ttu-id="1f273-313">\_ \_ \_ поле повторения отметки видео \_</span><span class="sxs-lookup"><span data-stu-id="1f273-313">AM\_VIDEO\_FLAG\_REPEAT\_FIELD</span></span>      | <span data-ttu-id="1f273-314">**Мфсампликстенсион \_ Репеатфирстфиелд**  =  **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1f273-314">**MFSampleExtension\_RepeatFirstField** = **TRUE**.</span></span> <span data-ttu-id="1f273-315">Если \_ \_ \_ отсутствует флаг поля повторения для флага видео \_ , установите для этого атрибута **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1f273-315">If the AM\_VIDEO\_FLAG\_REPEAT\_FIELD flag is not present, set this attribute to **FALSE**.</span></span>                                    |



 

<span data-ttu-id="1f273-316">Если образец DirectShow не содержит флаги выборки, используйте значение **двинтерлацефлагс** из структуры **VIDEOINFOHEADER2** :</span><span class="sxs-lookup"><span data-stu-id="1f273-316">If the DirectShow sample does not contain sample flags, use the value of **dwInterlaceFlags** from the **VIDEOINFOHEADER2** structure:</span></span>



| <span data-ttu-id="1f273-317">Флаг чередования DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f273-317">DirectShow interlace flag</span></span>    | <span data-ttu-id="1f273-318">Пример атрибута Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f273-318">Media Foundation sample attribute</span></span>                    |
|------------------------------|------------------------------------------------------|
| <span data-ttu-id="1f273-319">АМИНТЕРЛАЦЕ с \_ чередованием</span><span class="sxs-lookup"><span data-stu-id="1f273-319">AMINTERLACE\_IsInterlaced</span></span>    | <span data-ttu-id="1f273-320">**Мфсампликстенсион \_ С чередованием**  =  .</span><span class="sxs-lookup"><span data-stu-id="1f273-320">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span>        |
| <span data-ttu-id="1f273-321">АМИНТЕРЛАЦЕ \_ 1FieldPerSample</span><span class="sxs-lookup"><span data-stu-id="1f273-321">AMINTERLACE\_1FieldPerSample</span></span> | <span data-ttu-id="1f273-322">**Мфсампликстенсион \_ Синглефиелд**  =  **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1f273-322">**MFSampleExtension\_SingleField** = **TRUE**.</span></span>       |
| <span data-ttu-id="1f273-323">АМИНТЕРЛАЦЕ \_ Field1First</span><span class="sxs-lookup"><span data-stu-id="1f273-323">AMINTERLACE\_Field1First</span></span>     | <span data-ttu-id="1f273-324">**Мфсампликстенсион \_ Боттомфиелдфирст**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="1f273-324">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1f273-325">См. также</span><span class="sxs-lookup"><span data-stu-id="1f273-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f273-326">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="1f273-326">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="1f273-327">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="1f273-327">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




