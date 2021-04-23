---
description: Следующие идентификаторы GUID определяют категории для Media Foundation преобразований (МФТС). Эти категории используются для регистрации и перечисления МФТС.
ms.assetid: eca3ae3b-e40a-407d-986c-d0a85b891f52
title: MFT_CATEGORY (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7bc74054ad9f201b1f2ca53b526826d34c510d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898733"
---
# <a name="mft_category"></a><span data-ttu-id="d4d0f-104">\_Категория MFT</span><span class="sxs-lookup"><span data-stu-id="d4d0f-104">MFT\_CATEGORY</span></span>

<span data-ttu-id="d4d0f-105">Следующие идентификаторы GUID определяют категории для Media Foundation преобразований (МФТС).</span><span class="sxs-lookup"><span data-stu-id="d4d0f-105">The following GUIDs define categories for Media Foundation transforms (MFTs).</span></span> <span data-ttu-id="d4d0f-106">Эти категории используются для регистрации и перечисления МФТС.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-106">These categories are used to register and enumerate MFTs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="d4d0f-107">Константа</span><span class="sxs-lookup"><span data-stu-id="d4d0f-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d4d0f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d4d0f-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl> <span data-ttu-id="d4d0f-109"><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4d0f-109"><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d4d0f-110">Звуковые декодеры.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-110">Audio decoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl> <span data-ttu-id="d4d0f-111"><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4d0f-111"><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d4d0f-112">Звуковые эффекты.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-112">Audio effects.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl> <span data-ttu-id="d4d0f-113"><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4d0f-113"><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d4d0f-114">Звуковые кодировщики.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-114">Audio encoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl> <span data-ttu-id="d4d0f-115"><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4d0f-115"><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d4d0f-116">Демультиплексоры.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-116">Demultiplexers.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl> <span data-ttu-id="d4d0f-117"><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4d0f-117"><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d4d0f-118">Мультиплексоры.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-118">Multiplexers.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d4d0f-119">В Windows Vista конвейер Media Foundation не поддерживает МФТС с более чем одним входом.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-119">In Windows Vista, the Media Foundation pipeline does not support MFTs with more than one input.</span></span> <span data-ttu-id="d4d0f-120">В Windows 7 поддерживаются множественные входные МФТС.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-120">Multiple-input MFTs are supported in Windows 7.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl> <span data-ttu-id="d4d0f-121"><dt><strong>MFT_CATEGORY_OTHER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4d0f-121"><dt><strong>MFT_CATEGORY_OTHER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d4d0f-122">Прочие МФТС.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-122">Miscellaneous MFTs.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl> <span data-ttu-id="d4d0f-123"><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4d0f-123"><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d4d0f-124">Видеодекодеры.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-124">Video decoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl> <span data-ttu-id="d4d0f-125"><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4d0f-125"><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d4d0f-126">Видеоэффекты.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-126">Video effects.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl> <span data-ttu-id="d4d0f-127"><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4d0f-127"><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d4d0f-128">Эффекты модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-128">Video renderer effects.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl> <span data-ttu-id="d4d0f-129"><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4d0f-129"><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d4d0f-130">Видеокодировщики.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-130">Video encoders.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl> <span data-ttu-id="d4d0f-131"><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d4d0f-131"><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="d4d0f-132">Впервые появился в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-132">Introduced in Windows 7.</span></span>
</blockquote>
<br/> <span data-ttu-id="d4d0f-133">Обработчики видео.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-133">Video processors.</span></span> <br/> <span data-ttu-id="d4d0f-134">Эта категория ограничена МФТС, которая выполняет преобразования формата в несжатом видео, включая преобразования цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="d4d0f-134">This category is limited to MFTs that perform format conversions on uncompressed video, including color-space conversions.</span></span> <span data-ttu-id="d4d0f-135">Для видеоэффектов, изменяющих внешний вид изображения (например, эффект размытия или преобразование цветов в оттенки серого), используйте категорию <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4d0f-135">For video effects that modify the appearance of the image (such as a blur effect or a color-to-grayscale transform), use the <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> category.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="d4d0f-136">Требования</span><span class="sxs-lookup"><span data-stu-id="d4d0f-136">Requirements</span></span>



| <span data-ttu-id="d4d0f-137">Требование</span><span class="sxs-lookup"><span data-stu-id="d4d0f-137">Requirement</span></span> | <span data-ttu-id="d4d0f-138">Значение</span><span class="sxs-lookup"><span data-stu-id="d4d0f-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d0f-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4d0f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d0f-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4d0f-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d4d0f-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4d0f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d0f-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d4d0f-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d4d0f-143">Header</span><span class="sxs-lookup"><span data-stu-id="d4d0f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4d0f-144"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d0f-144"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d0f-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4d0f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d0f-146">Константы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d4d0f-146">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="d4d0f-147">Преобразования Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d4d0f-147">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="d4d0f-148">**мфтенум**</span><span class="sxs-lookup"><span data-stu-id="d4d0f-148">**MFTEnum**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
</dt> <dt>

[<span data-ttu-id="d4d0f-149">**мфтенумекс**</span><span class="sxs-lookup"><span data-stu-id="d4d0f-149">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> <dt>

[<span data-ttu-id="d4d0f-150">**мфтрегистер**</span><span class="sxs-lookup"><span data-stu-id="d4d0f-150">**MFTRegister**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
</dt> </dl>

 

 




