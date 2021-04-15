---
description: Для видео DV определено несколько подтипов. У каждого есть код FOURCC и соответствующее значение идентификатора GUID. Поддерживаются не все форматы. Дополнительные сведения см. в разделе "Примечания".
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: Подтипы видео DV (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676048"
---
# <a name="dv-video-subtypes"></a><span data-ttu-id="c8414-105">Подтипы видео DV</span><span class="sxs-lookup"><span data-stu-id="c8414-105">DV Video Subtypes</span></span>

<span data-ttu-id="c8414-106">Для видео DV определено несколько подтипов.</span><span class="sxs-lookup"><span data-stu-id="c8414-106">A number of subtypes are defined for DV video.</span></span> <span data-ttu-id="c8414-107">У каждого есть код FOURCC и соответствующее значение идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="c8414-107">Each has a FOURCC code and a corresponding GUID value.</span></span> <span data-ttu-id="c8414-108">Поддерживаются не все форматы. Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="c8414-108">Not all of these formats are supported; see the Remarks section for more information.</span></span>

## <a name="consumer-formats"></a><span data-ttu-id="c8414-109">Форматы потребителей</span><span class="sxs-lookup"><span data-stu-id="c8414-109">Consumer Formats</span></span>



| <span data-ttu-id="c8414-110">FOURCC</span><span class="sxs-lookup"><span data-stu-id="c8414-110">FOURCC</span></span> | <span data-ttu-id="c8414-111">Код GUID</span><span class="sxs-lookup"><span data-stu-id="c8414-111">GUID</span></span>               | <span data-ttu-id="c8414-112">Скорость передачи данных</span><span class="sxs-lookup"><span data-stu-id="c8414-112">Data Rate</span></span> | <span data-ttu-id="c8414-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c8414-113">Description</span></span>                  |
|--------|--------------------|-----------|------------------------------|
| <span data-ttu-id="c8414-114">"двсл"</span><span class="sxs-lookup"><span data-stu-id="c8414-114">'dvsl'</span></span> | <span data-ttu-id="c8414-115">МЕДИАСУБТИПЕ \_ двсл</span><span class="sxs-lookup"><span data-stu-id="c8414-115">MEDIASUBTYPE\_dvsl</span></span> | <span data-ttu-id="c8414-116">12,5 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="c8414-116">12.5 Mbps</span></span> | <span data-ttu-id="c8414-117">SD-ДВКР (525-60 или 625-50)</span><span class="sxs-lookup"><span data-stu-id="c8414-117">SD-DVCR (525-60 or 625-50)</span></span>   |
| <span data-ttu-id="c8414-118">"двсд"</span><span class="sxs-lookup"><span data-stu-id="c8414-118">'dvsd'</span></span> | <span data-ttu-id="c8414-119">МЕДИАСУБТИПЕ \_ двсд</span><span class="sxs-lookup"><span data-stu-id="c8414-119">MEDIASUBTYPE\_dvsd</span></span> | <span data-ttu-id="c8414-120">25 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="c8414-120">25 Mbps</span></span>   | <span data-ttu-id="c8414-121">SDL-ДВКР (525-60 или 625-50)</span><span class="sxs-lookup"><span data-stu-id="c8414-121">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="c8414-122">"двхд"</span><span class="sxs-lookup"><span data-stu-id="c8414-122">'dvhd'</span></span> | <span data-ttu-id="c8414-123">МЕДИАСУБТИПЕ \_ двхд</span><span class="sxs-lookup"><span data-stu-id="c8414-123">MEDIASUBTYPE\_dvhd</span></span> | <span data-ttu-id="c8414-124">50 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="c8414-124">50 Mbps</span></span>   | <span data-ttu-id="c8414-125">HD-ДВКР (1125-60 или 1250-50)</span><span class="sxs-lookup"><span data-stu-id="c8414-125">HD-DVCR (1125-60 or 1250-50)</span></span> |



 

<span data-ttu-id="c8414-126">Дополнительные сведения об этих форматах см. в статье IEC-61834.</span><span class="sxs-lookup"><span data-stu-id="c8414-126">Refer to IEC-61834 for more information about these formats.</span></span>

## <a name="professional-formats"></a><span data-ttu-id="c8414-127">Профессиональные форматы</span><span class="sxs-lookup"><span data-stu-id="c8414-127">Professional Formats</span></span>



| <span data-ttu-id="c8414-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="c8414-128">FOURCC</span></span> | <span data-ttu-id="c8414-129">Код GUID</span><span class="sxs-lookup"><span data-stu-id="c8414-129">GUID</span></span>               | <span data-ttu-id="c8414-130">Скорость передачи данных</span><span class="sxs-lookup"><span data-stu-id="c8414-130">Data Rate</span></span> | <span data-ttu-id="c8414-131">Описание</span><span class="sxs-lookup"><span data-stu-id="c8414-131">Description</span></span>                                 |
|--------|--------------------|-----------|---------------------------------------------|
| <span data-ttu-id="c8414-132">'dv25'</span><span class="sxs-lookup"><span data-stu-id="c8414-132">'dv25'</span></span> | <span data-ttu-id="c8414-133">МЕДИАСУБТИПЕ \_ DV25</span><span class="sxs-lookup"><span data-stu-id="c8414-133">MEDIASUBTYPE\_dv25</span></span> | <span data-ttu-id="c8414-134">25 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="c8414-134">25 Mbps</span></span>   | <span data-ttu-id="c8414-135">DVCPRO 25 (525-60 или 625-50).</span><span class="sxs-lookup"><span data-stu-id="c8414-135">DVCPRO 25 (525-60 or 625-50).</span></span>               |
| <span data-ttu-id="c8414-136">'dv50'</span><span class="sxs-lookup"><span data-stu-id="c8414-136">'dv50'</span></span> | <span data-ttu-id="c8414-137">МЕДИАСУБТИПЕ \_ DV50</span><span class="sxs-lookup"><span data-stu-id="c8414-137">MEDIASUBTYPE\_dv50</span></span> | <span data-ttu-id="c8414-138">50 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="c8414-138">50 Mbps</span></span>   | <span data-ttu-id="c8414-139">DVCPRO 50 (525-60 или 625-50)</span><span class="sxs-lookup"><span data-stu-id="c8414-139">DVCPRO 50 (525-60 or 625-50)</span></span>                |
| <span data-ttu-id="c8414-140">'dvh1'</span><span class="sxs-lookup"><span data-stu-id="c8414-140">'dvh1'</span></span> | <span data-ttu-id="c8414-141">МЕДИАСУБТИПЕ \_ dvh1</span><span class="sxs-lookup"><span data-stu-id="c8414-141">MEDIASUBTYPE\_dvh1</span></span> | <span data-ttu-id="c8414-142">100 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="c8414-142">100 Mbps</span></span>  | <span data-ttu-id="c8414-143">DVCPRO 100 (1080/60i, 1080/50i или 720/60P)</span><span class="sxs-lookup"><span data-stu-id="c8414-143">DVCPRO 100 (1080/60i, 1080/50i, or 720/60P)</span></span> |



 

<span data-ttu-id="c8414-144">Дополнительные сведения о DV25 и DV50 и SMPTE 370M для получения дополнительных сведений о dvh1 см. в разделе SMPTE 314M.</span><span class="sxs-lookup"><span data-stu-id="c8414-144">Refer to SMPTE 314M for more information about dv25 and dv50, and SMPTE 370M for more information about dvh1.</span></span>

## <a name="miscellaneous"></a><span data-ttu-id="c8414-145">Разное</span><span class="sxs-lookup"><span data-stu-id="c8414-145">Miscellaneous</span></span>

<span data-ttu-id="c8414-146">Два дополнительных подтипа DV определены в файле заголовков UUID. h.</span><span class="sxs-lookup"><span data-stu-id="c8414-146">Two additional DV subtypes are defined in the header file Uuids.h.</span></span> <span data-ttu-id="c8414-147">Они соответствуют кодам FOURCC, формируемым определенными кодеками DV; они не соответствуют ни одному из заданных стандартов DV.</span><span class="sxs-lookup"><span data-stu-id="c8414-147">These correspond to FOURCC codes that are produced by certain DV codecs; they do not correspond to any defined DV standards.</span></span> <span data-ttu-id="c8414-148">Эти подтипы являются устаревшими и не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="c8414-148">These subtypes are obsolete and should not be used.</span></span>



| <span data-ttu-id="c8414-149">FOURCC</span><span class="sxs-lookup"><span data-stu-id="c8414-149">FOURCC</span></span> | <span data-ttu-id="c8414-150">Код GUID</span><span class="sxs-lookup"><span data-stu-id="c8414-150">GUID</span></span>               |
|--------|--------------------|
| <span data-ttu-id="c8414-151">DVCS</span><span class="sxs-lookup"><span data-stu-id="c8414-151">'DVCS'</span></span> | <span data-ttu-id="c8414-152">МЕДИАСУБТИПЕ \_ DVCS</span><span class="sxs-lookup"><span data-stu-id="c8414-152">MEDIASUBTYPE\_DVCS</span></span> |
| <span data-ttu-id="c8414-153">"ДВСД"</span><span class="sxs-lookup"><span data-stu-id="c8414-153">'DVSD'</span></span> | <span data-ttu-id="c8414-154">МЕДИАСУБТИПЕ \_ двсд</span><span class="sxs-lookup"><span data-stu-id="c8414-154">MEDIASUBTYPE\_DVSD</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c8414-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8414-155">Remarks</span></span>

<span data-ttu-id="c8414-156">В следующей таблице приведены поддерживаемые скорости передачи данных в мегабит в секунду (Мбит/с) для драйверов МСДВ и УВК.</span><span class="sxs-lookup"><span data-stu-id="c8414-156">The following table shows the supported data rates, in megabits per second (Mbps), for the MSDV and UVC drivers.</span></span>



| <span data-ttu-id="c8414-157">Операционная система</span><span class="sxs-lookup"><span data-stu-id="c8414-157">Operating System</span></span>                                                                 | <span data-ttu-id="c8414-158">Драйвер МСДВ (IEEE 1394)</span><span class="sxs-lookup"><span data-stu-id="c8414-158">MSDV (IEEE 1394) Driver</span></span> | <span data-ttu-id="c8414-159">Драйвер УВК</span><span class="sxs-lookup"><span data-stu-id="c8414-159">UVC Driver</span></span>    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| <span data-ttu-id="c8414-160">Windows XP с пакетом обновления 1 или более ранней версии</span><span class="sxs-lookup"><span data-stu-id="c8414-160">Windows XP Service Pack 1 or earlier</span></span>                                             | <span data-ttu-id="c8414-161">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="c8414-161">12.5, 25</span></span>                | <span data-ttu-id="c8414-162">Недоступно</span><span class="sxs-lookup"><span data-stu-id="c8414-162">Not available</span></span> |
| <span data-ttu-id="c8414-163">Windows XP с пакетом обновления 2 или более поздней версии, Windows Server 2003 с пакетом обновления 1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c8414-163">Windows XP Service Pack 2 or later, Windows Server 2003 Service Pack 1 or later.</span></span> | <span data-ttu-id="c8414-164">12,5, 25, 50, 100</span><span class="sxs-lookup"><span data-stu-id="c8414-164">12.5, 25, 50, 100</span></span>       | <span data-ttu-id="c8414-165">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="c8414-165">12.5, 25</span></span>      |



 

<span data-ttu-id="c8414-166">В случае с потоками по 25 Мбит/с в Windows Vista, существовавшем до Windows Vista, драйвер МСДВ всегда установил тип носителя в МЕДИАСУБТИПЕ \_ двсд для потоков с 25 Мбит/с, независимо от того, был ли источник SDL-двкр или DVCPRO 25.</span><span class="sxs-lookup"><span data-stu-id="c8414-166">For 25-Mbps streams, the behavior of the MSDV driver has changed in Windows Vista Prior to Windows Vista, the MSDV driver always set the media type to MEDIASUBTYPE\_dvsd for 25-Mbps streams, regardless of whether the source was SDL-DVCR or DVCPRO 25.</span></span> <span data-ttu-id="c8414-167">Тип носителя "DV25" не использовался.</span><span class="sxs-lookup"><span data-stu-id="c8414-167">The 'dv25' media type was not used.</span></span> <span data-ttu-id="c8414-168">Начиная с Windows Vista, драйвер МСДВ теперь различает эти два формата.</span><span class="sxs-lookup"><span data-stu-id="c8414-168">Starting with Windows Vista, the MSDV driver now distinguishes between these two formats.</span></span> <span data-ttu-id="c8414-169">Для SDL-ДВКР будет использоваться подтип "двсд".</span><span class="sxs-lookup"><span data-stu-id="c8414-169">For SDL-DVCR, it continues to use the 'dvsd' subtype.</span></span> <span data-ttu-id="c8414-170">Для DVCPRO 25 теперь используется подтип «DV25».</span><span class="sxs-lookup"><span data-stu-id="c8414-170">For DVCPRO 25, it now uses the 'dv25' subtype.</span></span>

<span data-ttu-id="c8414-171">Фильтры видео- [разделителя](dv-splitter-filter.md) DirectShow и [видеодекодера формата DV](dv-video-decoder-filter.md) поддерживают только форматы SDL-двкр.</span><span class="sxs-lookup"><span data-stu-id="c8414-171">The DirectShow [DV Splitter](dv-splitter-filter.md) and [DV Video Decoder](dv-video-decoder-filter.md) filters support SDL-DVCR formats only.</span></span> <span data-ttu-id="c8414-172">Данные могут быть PAL или NTSC.</span><span class="sxs-lookup"><span data-stu-id="c8414-172">The data can be PAL or NTSC.</span></span> <span data-ttu-id="c8414-173">Могут быть доступны сторонние фильтры или кодеки, которые могут анализировать другие форматы DV, если скорость передачи данных поддерживается драйвером МСДВ или УВК.</span><span class="sxs-lookup"><span data-stu-id="c8414-173">Third-party filters or codecs may be available that can parse other DV formats, as long as the data rate is supported by the MSDV or UVC driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8414-174">Требования</span><span class="sxs-lookup"><span data-stu-id="c8414-174">Requirements</span></span>



| <span data-ttu-id="c8414-175">Требование</span><span class="sxs-lookup"><span data-stu-id="c8414-175">Requirement</span></span> | <span data-ttu-id="c8414-176">Значение</span><span class="sxs-lookup"><span data-stu-id="c8414-176">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8414-177">Header</span><span class="sxs-lookup"><span data-stu-id="c8414-177">Header</span></span><br/> | <dl> <span data-ttu-id="c8414-178"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8414-178"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8414-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8414-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8414-180">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="c8414-180">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="c8414-181">Драйвер МСДВ</span><span class="sxs-lookup"><span data-stu-id="c8414-181">MSDV Driver</span></span>](msdv-driver.md)
</dt> <dt>

[<span data-ttu-id="c8414-182">Подтипы видео</span><span class="sxs-lookup"><span data-stu-id="c8414-182">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




