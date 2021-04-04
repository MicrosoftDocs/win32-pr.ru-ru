---
description: Типы видео H. 264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Типы видео H. 264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd33703798e305947cdcd663c7a86c7c494683
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103989891"
---
# <a name="h264-video-types"></a><span data-ttu-id="39220-103">Типы видео H. 264</span><span class="sxs-lookup"><span data-stu-id="39220-103">H.264 Video Types</span></span>

<span data-ttu-id="39220-104">Для видео H. 264 определены следующие подтипы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="39220-104">The following media subtypes are defined for H.264 video.</span></span>



| <span data-ttu-id="39220-105">Subtype</span><span class="sxs-lookup"><span data-stu-id="39220-105">Subtype</span></span>                | <span data-ttu-id="39220-106">FOURCC</span><span class="sxs-lookup"><span data-stu-id="39220-106">FOURCC</span></span> | <span data-ttu-id="39220-107">Описание</span><span class="sxs-lookup"><span data-stu-id="39220-107">Description</span></span>                                                    |
|------------------------|--------|----------------------------------------------------------------|
| <span data-ttu-id="39220-108">**МЕДИАСУБТИПЕ \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="39220-108">**MEDIASUBTYPE\_AVC1**</span></span> | <span data-ttu-id="39220-109">'AVC1'</span><span class="sxs-lookup"><span data-stu-id="39220-109">'AVC1'</span></span> | <span data-ttu-id="39220-110">H. 264 битовый поток без начальных кодов.</span><span class="sxs-lookup"><span data-stu-id="39220-110">H.264 bitstream without start codes.</span></span>                           |
| <span data-ttu-id="39220-111">**МЕДИАСУБТИПЕ \_ H264 Single bitrate**</span><span class="sxs-lookup"><span data-stu-id="39220-111">**MEDIASUBTYPE\_H264**</span></span> | <span data-ttu-id="39220-112">H264 Single bitrate</span><span class="sxs-lookup"><span data-stu-id="39220-112">'H264'</span></span> | <span data-ttu-id="39220-113">H. 264 битовый поток с начальными кодами.</span><span class="sxs-lookup"><span data-stu-id="39220-113">H.264 bitstream with start codes.</span></span>                              |
| <span data-ttu-id="39220-114">**МЕДИАСУБТИПЕ \_ H264 Single bitrate**</span><span class="sxs-lookup"><span data-stu-id="39220-114">**MEDIASUBTYPE\_h264**</span></span> | <span data-ttu-id="39220-115">H264 Single bitrate</span><span class="sxs-lookup"><span data-stu-id="39220-115">'h264'</span></span> | <span data-ttu-id="39220-116">Эквивалентно **медиасубтипе \_ H264 Single bitrate** с другим FourCC.</span><span class="sxs-lookup"><span data-stu-id="39220-116">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="39220-117">**МЕДИАСУБТИПЕ \_ X264**</span><span class="sxs-lookup"><span data-stu-id="39220-117">**MEDIASUBTYPE\_X264**</span></span> | <span data-ttu-id="39220-118">'X264'</span><span class="sxs-lookup"><span data-stu-id="39220-118">'X264'</span></span> | <span data-ttu-id="39220-119">Эквивалентно **медиасубтипе \_ H264 Single bitrate** с другим FourCC.</span><span class="sxs-lookup"><span data-stu-id="39220-119">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="39220-120">**МЕДИАСУБТИПЕ \_ x264**</span><span class="sxs-lookup"><span data-stu-id="39220-120">**MEDIASUBTYPE\_x264**</span></span> | <span data-ttu-id="39220-121">'x264'</span><span class="sxs-lookup"><span data-stu-id="39220-121">'x264'</span></span> | <span data-ttu-id="39220-122">Эквивалентно **медиасубтипе \_ H264 Single bitrate** с другим FourCC.</span><span class="sxs-lookup"><span data-stu-id="39220-122">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |



 

<span data-ttu-id="39220-123">Эти идентификаторы GUID подтипа объявляются в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="39220-123">These subtype GUIDs are declared in wmcodecdsp.h.</span></span>

<span data-ttu-id="39220-124">Основное различие между этими типами носителей заключается в наличии начальных кодов в битовый поток.</span><span class="sxs-lookup"><span data-stu-id="39220-124">The main difference between these media types is the presence of start codes in the bitstream.</span></span> <span data-ttu-id="39220-125">Если подтип имеет значение **медиасубтипе \_ AVC1**, битовый поток не содержит начальных кодов.</span><span class="sxs-lookup"><span data-stu-id="39220-125">If the subtype is **MEDIASUBTYPE\_AVC1**, the bitstream does not contain start codes.</span></span>

### <a name="h264-bitstream-with-start-codes"></a><span data-ttu-id="39220-126">H. 264 битовый поток с начальными кодами</span><span class="sxs-lookup"><span data-stu-id="39220-126">H.264 Bitstream with Start Codes</span></span>

<span data-ttu-id="39220-127">H. 264 битстреамс, передаваемые по воздуху или содержащиеся в программе MPEG-2 или в потоках транспорта или записанных на HD-DVD, форматируются в соответствии с описанием в приложении B из ITU-T Rec. H. 264.</span><span class="sxs-lookup"><span data-stu-id="39220-127">H.264 bitstreams that are transmitted over the air, or contained in MPEG-2 program or transport streams, or recorded on HD-DVD, are formatted as described in Annex B of ITU-T Rec. H.264.</span></span> <span data-ttu-id="39220-128">В соответствии с этой спецификацией битовый поток состоит из последовательности единиц уровня абстракции сети (Налус), каждый из которых имеет префикс начального кода, равный 0x000001 или 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="39220-128">According to this specification, the bitstream consists of a sequence of network abstraction layer units (NALUs), each of which is prefixed with a start code equal to 0x000001 or 0x00000001.</span></span>

<span data-ttu-id="39220-129">Если в битовый поток имеются начальные коды, используется следующий тип носителя:</span><span class="sxs-lookup"><span data-stu-id="39220-129">When start codes are present in the bitstream, the following media type is used:</span></span>



|             |                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39220-130">Основной тип</span><span class="sxs-lookup"><span data-stu-id="39220-130">Major type</span></span>  | <span data-ttu-id="39220-131">**\_Видео MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="39220-131">**MEDIATYPE\_Video**</span></span>                                                                              |
| <span data-ttu-id="39220-132">Подтипы</span><span class="sxs-lookup"><span data-stu-id="39220-132">Subtypes</span></span>    | <span data-ttu-id="39220-133">**Медиасубтипе \_ H264 Single bitrate**, **медиасубтипе \_ H264 Single bitrate**, **медиасубтипе \_ X264** или **медиасубтипе \_ X264**</span><span class="sxs-lookup"><span data-stu-id="39220-133">**MEDIASUBTYPE\_H264**, **MEDIASUBTYPE\_h264**, **MEDIASUBTYPE\_X264**, or **MEDIASUBTYPE\_x264**</span></span> |
| <span data-ttu-id="39220-134">Тип формата</span><span class="sxs-lookup"><span data-stu-id="39220-134">Format type</span></span> | <span data-ttu-id="39220-135">**Формат \_ Видеоинфо**, **Format \_ VideoInfo2**, **Format \_ MPEG2Video** или **GUID \_ null**</span><span class="sxs-lookup"><span data-stu-id="39220-135">**FORMAT\_VideoInfo**, **FORMAT\_VideoInfo2**, **FORMAT\_MPEG2Video**, or **GUID\_NULL**</span></span>          |



 

<span data-ttu-id="39220-136">Если тип формата — **GUID \_ null**, структура формата отсутствует.</span><span class="sxs-lookup"><span data-stu-id="39220-136">If the format type is **GUID\_NULL**, no format structure is present.</span></span>

<span data-ttu-id="39220-137">Если битовый поток содержит начальные коды, все типы форматов, перечисленные здесь, достаточно, поскольку декодеру не требуются дополнительные сведения для синтаксического анализа потока.</span><span class="sxs-lookup"><span data-stu-id="39220-137">When the bitstream contains start codes, any of the format types listed here is sufficient, because the decoder does not require any additional information to parse the stream.</span></span> <span data-ttu-id="39220-138">Битовый поток уже содержит всю информацию, необходимую декодеру, а коды запуска позволяют декодеру определять начало каждого налу.</span><span class="sxs-lookup"><span data-stu-id="39220-138">The bitstream already contains all of the information needed by the decoder, and the start codes enable the decoder to locate the start of each NALU.</span></span>

<span data-ttu-id="39220-139">Следующие подтипы эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="39220-139">The following subtypes are equivalent:</span></span>

### <a name="h264-bitstream-without-start-codes"></a><span data-ttu-id="39220-140">H. 264 битовый поток без начальных кодов</span><span class="sxs-lookup"><span data-stu-id="39220-140">H.264 Bitstream Without Start Codes</span></span>

<span data-ttu-id="39220-141">Формат контейнера MP4 хранит данные H. 264 без начальных кодов.</span><span class="sxs-lookup"><span data-stu-id="39220-141">The MP4 container format stores H.264 data without start codes.</span></span> <span data-ttu-id="39220-142">Вместо этого каждый налу имеет префикс в поле длины, который задает длину налу в байтах.</span><span class="sxs-lookup"><span data-stu-id="39220-142">Instead, each NALU is prefixed by a length field, which gives the length of the NALU in bytes.</span></span> <span data-ttu-id="39220-143">Размер поля Длина может быть разным, но обычно это 1, 2 или 4 байта.</span><span class="sxs-lookup"><span data-stu-id="39220-143">The size of the length field can vary, but is typically 1, 2, or 4 bytes.</span></span>

<span data-ttu-id="39220-144">Если в битовый поток отсутствуют начальные коды, используется следующий тип носителя.</span><span class="sxs-lookup"><span data-stu-id="39220-144">When start codes are not present in the bitstream, the following media type is used.</span></span>



|             |                        |
|-------------|------------------------|
| <span data-ttu-id="39220-145">Основной тип</span><span class="sxs-lookup"><span data-stu-id="39220-145">Major type</span></span>  | <span data-ttu-id="39220-146">**\_Видео MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="39220-146">**MEDIATYPE\_Video**</span></span>   |
| <span data-ttu-id="39220-147">Subtype</span><span class="sxs-lookup"><span data-stu-id="39220-147">Subtype</span></span>     | <span data-ttu-id="39220-148">**МЕДИАСУБТИПЕ \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="39220-148">**MEDIASUBTYPE\_AVC1**</span></span> |
| <span data-ttu-id="39220-149">Тип формата</span><span class="sxs-lookup"><span data-stu-id="39220-149">Format type</span></span> | <span data-ttu-id="39220-150">**ФОРМАТ \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="39220-150">**FORMAT\_MPEG2Video**</span></span> |



 

<span data-ttu-id="39220-151">Блок формата является структурой [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="39220-151">The format block is an [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="39220-152">Эта структура должна быть заполнена следующим образом:</span><span class="sxs-lookup"><span data-stu-id="39220-152">This structure should be filled in as follows:</span></span>

-   <span data-ttu-id="39220-153">**HDR**: структура [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , описывающая битовый поток.</span><span class="sxs-lookup"><span data-stu-id="39220-153">**hdr**: A [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure that describes the bitstream.</span></span> <span data-ttu-id="39220-154">После [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) части структуры отсутствует таблица цветов, а **биклрусед** должна быть равна нулю.</span><span class="sxs-lookup"><span data-stu-id="39220-154">No color table is present after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) portion of the structure, and **biClrUsed** must be zero.</span></span>
-   <span data-ttu-id="39220-155">**двстарттимекоде**: не используется.</span><span class="sxs-lookup"><span data-stu-id="39220-155">**dwStartTimeCode**: Not used.</span></span> <span data-ttu-id="39220-156">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="39220-156">Set to zero.</span></span>
-   <span data-ttu-id="39220-157">**кбсекуенцехеадер**: длина массива **двсекуенцехеадер** в байтах.</span><span class="sxs-lookup"><span data-stu-id="39220-157">**cbSequenceHeader**: The length of the **dwSequenceHeader** array in bytes.</span></span>
-   <span data-ttu-id="39220-158">**двпрофиле**: указывает профиль H. 264.</span><span class="sxs-lookup"><span data-stu-id="39220-158">**dwProfile**: Specifies the H.264 profile.</span></span>
-   <span data-ttu-id="39220-159">**двлевел**: указывает уровень H. 264.</span><span class="sxs-lookup"><span data-stu-id="39220-159">**dwLevel**: Specifies the H.264 level.</span></span>
-   <span data-ttu-id="39220-160">**dwFlags**: число байтов, используемых для поля length, которое появляется перед каждым **налу**.</span><span class="sxs-lookup"><span data-stu-id="39220-160">**dwFlags**: The number of bytes used for the length field that appears before each **NALU**.</span></span> <span data-ttu-id="39220-161">Поле Длина указывает размер следующего налу в байтах.</span><span class="sxs-lookup"><span data-stu-id="39220-161">The length field indicates the size of the following NALU in bytes.</span></span> <span data-ttu-id="39220-162">Например, если **dwFlags** имеет значение 4, то каждому налуу предшествует 4-байтовое поле длины.</span><span class="sxs-lookup"><span data-stu-id="39220-162">For example, if **dwFlags** is 4, each NALU is preceded by a 4-byte length field.</span></span> <span data-ttu-id="39220-163">Допустимые значения: 1, 2 и 4.</span><span class="sxs-lookup"><span data-stu-id="39220-163">The valid values are 1, 2, and 4.</span></span>
-   <span data-ttu-id="39220-164">**двсекуенцехеадер**: массив байтов, который может содержать набор параметров последовательности (SPS) и набор параметров Picture (PPS) налус.</span><span class="sxs-lookup"><span data-stu-id="39220-164">**dwSequenceHeader**: A byte array that may contain sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

<span data-ttu-id="39220-165">Контейнер MP4 может содержать наборы параметров последовательности (SPS) или наборы параметров изображений (PPS) в виде специальных единиц NAL в заголовках файлов или в отдельном потоке (отличном от видеопотока).</span><span class="sxs-lookup"><span data-stu-id="39220-165">The MP4 container might contain sequence parameter sets (SPS) or picture parameter sets (PPS) as special NAL units in file headers or in a separate stream (distinct from the video stream).</span></span> <span data-ttu-id="39220-166">При установке формата тип носителя может указывать единицы SPS и PPS NAL в массиве **двсекуенцехеадер** .</span><span class="sxs-lookup"><span data-stu-id="39220-166">When the format is established, the media type can specify SPS and PPS NAL units in the **dwSequenceHeader** array.</span></span> <span data-ttu-id="39220-167">Если **кбсекуенцехеадер** больше нуля, **двсекуенцехеадер** является началом массива байтов, содержащего SPS и PPS налус, разделенных полями длиной в 2 байта, все в сетевом порядке байтов (Big-endian).</span><span class="sxs-lookup"><span data-stu-id="39220-167">If **cbSequenceHeader** is greater than zero, **dwSequenceHeader** is the start of a byte array containing SPS and PPS NALUs, delimited by 2-byte length fields, all in network byte order (big-endian).</span></span> <span data-ttu-id="39220-168">Можно использовать как SPS, так и PPS, либо только один из этих типов, либо None.</span><span class="sxs-lookup"><span data-stu-id="39220-168">It is possible to have both SPS and PPS, only one of these types, or none.</span></span> <span data-ttu-id="39220-169">Реальный тип каждого налу можно определить с помощью проверки поля **\_ \_ типа "NAL** " в самом налу.</span><span class="sxs-lookup"><span data-stu-id="39220-169">The actual type of each NALU can be determined by examining the **nal\_unit\_type** field of the NALU itself.</span></span>

<span data-ttu-id="39220-170">При использовании этого типа носителя каждый пример носителя начинается в начале налу, а NAL-единицы не охватывают образцы.</span><span class="sxs-lookup"><span data-stu-id="39220-170">When this media type is used, each media sample starts at the beginning of a NALU, and NAL units do not span samples.</span></span> <span data-ttu-id="39220-171">Это позволяет декодеру восстанавливать данные из поврежденных или пропущенных примеров.</span><span class="sxs-lookup"><span data-stu-id="39220-171">This enables the decoder to recover from data corruption or dropped samples.</span></span>

 

 



