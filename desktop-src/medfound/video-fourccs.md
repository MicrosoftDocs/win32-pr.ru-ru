---
description: Видео Фаурккс
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: Видео Фаурккс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344852"
---
# <a name="video-fourccs"></a><span data-ttu-id="82df3-103">Видео Фаурккс</span><span class="sxs-lookup"><span data-stu-id="82df3-103">Video FOURCCs</span></span>

<span data-ttu-id="82df3-104">Для многих форматов видео назначены коды FOURCC.</span><span class="sxs-lookup"><span data-stu-id="82df3-104">Many video formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="82df3-105">Код FOURCC — это 32-разрядное целое число без знака, которое создается путем сцепления четырех символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="82df3-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="82df3-106">Например, код FOURCC для видео YUY2 — "YUY2".</span><span class="sxs-lookup"><span data-stu-id="82df3-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span>

<span data-ttu-id="82df3-107">Для объявления значений FOURCC в исходном коде определяются различные макросы C/C++.</span><span class="sxs-lookup"><span data-stu-id="82df3-107">Various C/C++ macros are defined for declaring FOURCC values in source code.</span></span> <span data-ttu-id="82df3-108">Макрос **макефауркк** определен в файле ммсистем. h, а макрос **FCC** определен в файле авирифф. h и различных других файлах заголовков.</span><span class="sxs-lookup"><span data-stu-id="82df3-108">The **MAKEFOURCC** macro is defined in Mmsystem.h, and the **FCC** macro is defined in Aviriff.h and various other header files.</span></span> <span data-ttu-id="82df3-109">Кроме того, можно объявить код FOURCC непосредственно в виде строкового литерала, просто отменив порядок символов.</span><span class="sxs-lookup"><span data-stu-id="82df3-109">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="82df3-110">Таким образом, следующие операторы эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="82df3-110">Thus, the following statements are equivalent:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

<span data-ttu-id="82df3-111">(В последнем примере обратный порядок байтов необходим, так как в Windows используется архитектура с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="82df3-111">(In the last example, reversing the byte order is necessary because Windows uses a little-endian architecture.</span></span> <span data-ttu-id="82df3-112">' Y ' = 0x59, ' U ' = 0x55, и ' 2 ' = 0x32, поэтому ' 2YUY ' является 0x32595559.)</span><span class="sxs-lookup"><span data-stu-id="82df3-112">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.)</span></span>

<span data-ttu-id="82df3-113">Некоторые API-интерфейсы [ускорения видео DirectX 2,0](directx-video-acceleration-2-0.md) используют значение **D3DFORMAT** для описания формата видео.</span><span class="sxs-lookup"><span data-stu-id="82df3-113">Some of the [DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md) APIs use a **D3DFORMAT** value to describe a video format.</span></span> <span data-ttu-id="82df3-114">В этом контексте можно также использовать код FOURCC:</span><span class="sxs-lookup"><span data-stu-id="82df3-114">A FOURCC code can be used in this context as well:</span></span>

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a><span data-ttu-id="82df3-115">Константы FOURCC</span><span class="sxs-lookup"><span data-stu-id="82df3-115">FOURCC Constants</span></span>

<span data-ttu-id="82df3-116">В следующей таблице перечислены некоторые распространенные коды FOURCC.</span><span class="sxs-lookup"><span data-stu-id="82df3-116">The following table lists some common FOURCC codes.</span></span>



| <span data-ttu-id="82df3-117">Значение FOURCC</span><span class="sxs-lookup"><span data-stu-id="82df3-117">FOURCC value</span></span> | <span data-ttu-id="82df3-118">Описание</span><span class="sxs-lookup"><span data-stu-id="82df3-118">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82df3-119">H264 Single bitrate</span><span class="sxs-lookup"><span data-stu-id="82df3-119">'H264'</span></span>       | <span data-ttu-id="82df3-120">Видео H. 264.</span><span class="sxs-lookup"><span data-stu-id="82df3-120">H.264 video.</span></span>                                                                                                          |
| <span data-ttu-id="82df3-121">'I420'</span><span class="sxs-lookup"><span data-stu-id="82df3-121">'I420'</span></span>       | <span data-ttu-id="82df3-122">Видео YUV, хранящееся в формате плоской 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="82df3-122">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="82df3-123">"ИЙУВ"</span><span class="sxs-lookup"><span data-stu-id="82df3-123">'IYUV'</span></span>       | <span data-ttu-id="82df3-124">Видео YUV, хранящееся в формате плоской 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="82df3-124">YUV video stored in planar 4:2:0 format.</span></span>                                                                              |
| <span data-ttu-id="82df3-125">«4S2»</span><span class="sxs-lookup"><span data-stu-id="82df3-125">'M4S2'</span></span>       | <span data-ttu-id="82df3-126">Видео MPEG-4 часть 2.</span><span class="sxs-lookup"><span data-stu-id="82df3-126">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="82df3-127">MP4 со МНОЖЕСТВЕННОЙ</span><span class="sxs-lookup"><span data-stu-id="82df3-127">'MP4S'</span></span>       | <span data-ttu-id="82df3-128">Кодек Microsoft MPEG 4, версия 3.</span><span class="sxs-lookup"><span data-stu-id="82df3-128">Microsoft MPEG 4 codec version 3.</span></span> <span data-ttu-id="82df3-129">Этот кодек больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="82df3-129">This codec is no longer supported.</span></span>                                                  |
| <span data-ttu-id="82df3-130">'MP4V'</span><span class="sxs-lookup"><span data-stu-id="82df3-130">'MP4V'</span></span>       | <span data-ttu-id="82df3-131">Видео MPEG-4 часть 2.</span><span class="sxs-lookup"><span data-stu-id="82df3-131">MPEG-4 part 2 video.</span></span>                                                                                                  |
| <span data-ttu-id="82df3-132">'MPG1'</span><span class="sxs-lookup"><span data-stu-id="82df3-132">'MPG1'</span></span>       | <span data-ttu-id="82df3-133">Видео MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="82df3-133">MPEG-1 video.</span></span>                                                                                                         |
| <span data-ttu-id="82df3-134">'MSS1'</span><span class="sxs-lookup"><span data-stu-id="82df3-134">'MSS1'</span></span>       | <span data-ttu-id="82df3-135">Содержимое, закодированное с помощью экранного видеокодека Windows Media Video 7.</span><span class="sxs-lookup"><span data-stu-id="82df3-135">Content encoded with the Windows Media Video 7 screen codec.</span></span>                                                          |
| <span data-ttu-id="82df3-136">'MSS2'</span><span class="sxs-lookup"><span data-stu-id="82df3-136">'MSS2'</span></span>       | <span data-ttu-id="82df3-137">Содержимое, закодированное с помощью экранного видеокодека Windows Media видео 9.</span><span class="sxs-lookup"><span data-stu-id="82df3-137">Content encoded with the Windows Media Video 9 screen codec.</span></span>                                                          |
| <span data-ttu-id="82df3-138">UYVY</span><span class="sxs-lookup"><span data-stu-id="82df3-138">'UYVY'</span></span>       | <span data-ttu-id="82df3-139">Видео YUV, хранящееся в упакованном формате 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="82df3-139">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="82df3-140">Аналогичен YUY2, но с различным порядком данных.</span><span class="sxs-lookup"><span data-stu-id="82df3-140">Similar to YUY2 but with different ordering of data.</span></span>                         |
| <span data-ttu-id="82df3-141">'WMV1'</span><span class="sxs-lookup"><span data-stu-id="82df3-141">'WMV1'</span></span>       | <span data-ttu-id="82df3-142">Содержимое, закодированное кодеком Windows Media Video 7.</span><span class="sxs-lookup"><span data-stu-id="82df3-142">Content encoded with the Windows Media Video 7 codec.</span></span>                                                                 |
| <span data-ttu-id="82df3-143">'WMV2'</span><span class="sxs-lookup"><span data-stu-id="82df3-143">'WMV2'</span></span>       | <span data-ttu-id="82df3-144">Содержимое, закодированное с помощью кодека Windows Media Video 8.</span><span class="sxs-lookup"><span data-stu-id="82df3-144">Content encoded with the Windows Media Video 8 codec.</span></span>                                                                 |
| <span data-ttu-id="82df3-145">'WMV3'</span><span class="sxs-lookup"><span data-stu-id="82df3-145">'WMV3'</span></span>       | <span data-ttu-id="82df3-146">Содержимое, закодированное кодеком Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="82df3-146">Content encoded with the Windows Media Video 9 codec.</span></span>                                                                 |
| <span data-ttu-id="82df3-147">"ВМВА"</span><span class="sxs-lookup"><span data-stu-id="82df3-147">'WMVA'</span></span>       | <span data-ttu-id="82df3-148">Содержимое, закодированное с помощью более старой, устаревшей версии кодека расширенного профиля Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="82df3-148">Content encoded with the older, obsolete version of the Windows Media Video 9 Advanced Profile codec.</span></span>                 |
| <span data-ttu-id="82df3-149">"ВМВП"</span><span class="sxs-lookup"><span data-stu-id="82df3-149">'WMVP'</span></span>       | <span data-ttu-id="82df3-150">Содержимое, закодированное с помощью кодека образа Windows Media Video 9,1.</span><span class="sxs-lookup"><span data-stu-id="82df3-150">Content encoded with the Windows Media Video 9.1 Image codec.</span></span>                                                         |
| <span data-ttu-id="82df3-151">'WVC1'</span><span class="sxs-lookup"><span data-stu-id="82df3-151">'WVC1'</span></span>       | <span data-ttu-id="82df3-152">SMPTE 421M ("VC-1").</span><span class="sxs-lookup"><span data-stu-id="82df3-152">SMPTE 421M ("VC-1").</span></span> <span data-ttu-id="82df3-153">Содержимое, закодированное с помощью расширенного профиля Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="82df3-153">Content encoded with Windows Media Video 9 Advanced Profile.</span></span>                                     |
| <span data-ttu-id="82df3-154">'WVP2'</span><span class="sxs-lookup"><span data-stu-id="82df3-154">'WVP2'</span></span>       | <span data-ttu-id="82df3-155">Содержимое, закодированное с помощью кодека Windows Media Video 9,1 Image v2.</span><span class="sxs-lookup"><span data-stu-id="82df3-155">Content encoded with the Windows Media Video 9.1 Image v2 codec.</span></span>                                                      |
| <span data-ttu-id="82df3-156">'YUY2'</span><span class="sxs-lookup"><span data-stu-id="82df3-156">'YUY2'</span></span>       | <span data-ttu-id="82df3-157">Видео YUV, хранящееся в упакованном формате 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="82df3-157">YUV video stored in packed 4:2:2 format.</span></span>                                                                              |
| <span data-ttu-id="82df3-158">'YV12'</span><span class="sxs-lookup"><span data-stu-id="82df3-158">'YV12'</span></span>       | <span data-ttu-id="82df3-159">Видео YUV, хранящееся в формате плоских 4:2:0 или 4:1:1.</span><span class="sxs-lookup"><span data-stu-id="82df3-159">YUV video stored in planar 4:2:0 or 4:1:1 format.</span></span> <span data-ttu-id="82df3-160">Аналогично I420/ИЙУВ, за исключением того, что вы и V перешли на плоскости.</span><span class="sxs-lookup"><span data-stu-id="82df3-160">Identical to I420/IYUV except that the U and V planes are switched.</span></span> |
| <span data-ttu-id="82df3-161">YVU9</span><span class="sxs-lookup"><span data-stu-id="82df3-161">'YVU9'</span></span>       | <span data-ttu-id="82df3-162">Видео YUV, хранящееся в формате плоской 16:1:1.</span><span class="sxs-lookup"><span data-stu-id="82df3-162">YUV video stored in planar 16:1:1 format.</span></span>                                                                             |
| <span data-ttu-id="82df3-163">"ИВЮ"</span><span class="sxs-lookup"><span data-stu-id="82df3-163">'YVYU'</span></span>       | <span data-ttu-id="82df3-164">Видео YUV, хранящееся в упакованном формате 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="82df3-164">YUV video stored in packed 4:2:2 format.</span></span> <span data-ttu-id="82df3-165">Аналогичен YUY2, но с различным порядком данных.</span><span class="sxs-lookup"><span data-stu-id="82df3-165">Similar to YUY2 but with different ordering of data.</span></span>                         |



 

## <a name="related-topics"></a><span data-ttu-id="82df3-166">См. также</span><span class="sxs-lookup"><span data-stu-id="82df3-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82df3-167">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="82df3-167">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="82df3-168">Идентификаторы GUID для подтипов видео</span><span class="sxs-lookup"><span data-stu-id="82df3-168">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



