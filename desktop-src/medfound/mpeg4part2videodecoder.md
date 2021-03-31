---
description: Видеодекодер MPEG4 часть 2 декодирует видеопотоки, закодированные в соответствии со стандартом MPEG4 (часть 2).
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: Видеодекодер MPEG-4 Part 2 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263510"
---
# <a name="mpeg-4-part-2-video-decoder"></a><span data-ttu-id="80dac-103">Видеодекодер MPEG-4 Part 2</span><span class="sxs-lookup"><span data-stu-id="80dac-103">MPEG-4 Part 2 Video Decoder</span></span>

<span data-ttu-id="80dac-104">Видеодекодер MPEG4 часть 2 декодирует видеопотоки, закодированные в соответствии со стандартом MPEG4 (часть 2).</span><span class="sxs-lookup"><span data-stu-id="80dac-104">The MPEG4 Part 2 Video decoder decodes video streams that were encoded according to the MPEG4 Part 2 standard.</span></span>

<span data-ttu-id="80dac-105">Вы можете создать экземпляр видеодекодера версии MPEG4 Part 2, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="80dac-105">You can create an instance of the MPEG4 Part 2 Video decoder by calling **CoCreateInstance**.</span></span> <span data-ttu-id="80dac-106">Чтобы создать экземпляр декодера, который ведет себя как объект мультимедиа DirectX (DMO), используйте идентификатор класса **CLSID \_ CMpeg4sDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="80dac-106">To create an instance of the decoder that behaves as a DirectX Media Object (DMO), use the class identifier **CLSID\_CMpeg4sDecMediaObject**.</span></span> <span data-ttu-id="80dac-107">Чтобы создать истанце декодера, который ведет себя как Media Foundation преобразование (MFT), используйте идентификатор класса **CLSID \_ CMpeg4sDecMFT**.</span><span class="sxs-lookup"><span data-stu-id="80dac-107">To create an istance of the decoder that behaves as a Media Foundation Transform (MFT), use the class identifier **CLSID\_CMpeg4sDecMFT**.</span></span>

## <a name="input-types"></a><span data-ttu-id="80dac-108">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="80dac-108">Input Types</span></span>

<span data-ttu-id="80dac-109">Видеодекодер MPEG4 Part 2 поддерживает следующие входные типы носителей.</span><span class="sxs-lookup"><span data-stu-id="80dac-109">The MPEG4 Part 2 Video decoder supports the following input media types.</span></span>

-   <span data-ttu-id="80dac-110">МЕДИАСУБТИПЕ \_ M4S2</span><span class="sxs-lookup"><span data-stu-id="80dac-110">MEDIASUBTYPE\_M4S2</span></span>
-   <span data-ttu-id="80dac-111">МЕДИАСУБТИПЕ \_ m4s2</span><span class="sxs-lookup"><span data-stu-id="80dac-111">MEDIASUBTYPE\_m4s2</span></span>
-   <span data-ttu-id="80dac-112">МЕДИАСУБТИПЕ \_ MP4V</span><span class="sxs-lookup"><span data-stu-id="80dac-112">MEDIASUBTYPE\_MP4V</span></span>
-   <span data-ttu-id="80dac-113">МЕДИАСУБТИПЕ \_ MP4V</span><span class="sxs-lookup"><span data-stu-id="80dac-113">MEDIASUBTYPE\_mp4v</span></span>
-   <span data-ttu-id="80dac-114">МЕДИАСУБТИПЕ \_ MP4 со множественной (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="80dac-114">MEDIASUBTYPE\_MP4S (deprecated)</span></span>
-   <span data-ttu-id="80dac-115">МЕДИАСУБТИПЕ \_ MP4 со множественной (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="80dac-115">MEDIASUBTYPE\_mp4s (deprecated)</span></span>

## <a name="output-types"></a><span data-ttu-id="80dac-116">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="80dac-116">Output Types</span></span>

<span data-ttu-id="80dac-117">Видеодекодер MPEG4 Part 2 поддерживает следующие выходные подтипы выходных данных, когда он выступает в роли DMO.</span><span class="sxs-lookup"><span data-stu-id="80dac-117">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="80dac-118">МЕДИАСУБТИПЕ \_ YV12</span><span class="sxs-lookup"><span data-stu-id="80dac-118">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="80dac-119">МЕДИАСУБТИПЕ \_ NV12</span><span class="sxs-lookup"><span data-stu-id="80dac-119">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="80dac-120">МЕДИАСУБТИПЕ \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="80dac-120">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="80dac-121">МЕДИАСУБТИПЕ \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="80dac-121">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="80dac-122">МЕДИАСУБТИПЕ \_ ивю</span><span class="sxs-lookup"><span data-stu-id="80dac-122">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="80dac-123">МЕДИАСУБТИПЕ \_ NV11</span><span class="sxs-lookup"><span data-stu-id="80dac-123">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="80dac-124">МЕДИАСУБТИПЕ \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="80dac-124">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="80dac-125">МЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="80dac-125">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="80dac-126">МЕДИАСУБТИПЕ \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="80dac-126">MEDIASUBTYPE\_ RGB565</span></span>
-   <span data-ttu-id="80dac-127">МЕДИАСУБТИПЕ \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="80dac-127">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="80dac-128">МЕДИАСУБТИПЕ \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="80dac-128">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="80dac-129">Видеодекодер MPEG4 Part 2 поддерживает следующие выходные типы выходных данных, когда он выступает в качестве MFT.</span><span class="sxs-lookup"><span data-stu-id="80dac-129">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="80dac-130">МЕДИАСУБТИПЕ \_ NV12</span><span class="sxs-lookup"><span data-stu-id="80dac-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="80dac-131">МЕДИАСУБТИПЕ \_ YV12</span><span class="sxs-lookup"><span data-stu-id="80dac-131">MEDIASUBTYPE\_YV12</span></span>

## <a name="formats"></a><span data-ttu-id="80dac-132">Форматы</span><span class="sxs-lookup"><span data-stu-id="80dac-132">Formats</span></span>

<span data-ttu-id="80dac-133">Видеодекодер MPEG4 Part 2 принимает следующие форматы.</span><span class="sxs-lookup"><span data-stu-id="80dac-133">The MPEG4 Part 2 Video decoder accepts the following formats.</span></span>

-   [<span data-ttu-id="80dac-134">**видеоинфохеадер**</span><span class="sxs-lookup"><span data-stu-id="80dac-134">**VIDEOINFOHEADER**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   <span data-ttu-id="80dac-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span><span class="sxs-lookup"><span data-stu-id="80dac-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span></span>
-   [<span data-ttu-id="80dac-136">**мфвидеоинфо**</span><span class="sxs-lookup"><span data-stu-id="80dac-136">**MFVideoInfo**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   <span data-ttu-id="80dac-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (используется только часть VIH2 заголовка).</span><span class="sxs-lookup"><span data-stu-id="80dac-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (Only the VIH2 portion of the header is used.)</span></span>

## <a name="interfaces-for-the-dmo"></a><span data-ttu-id="80dac-138">Интерфейсы DMO</span><span class="sxs-lookup"><span data-stu-id="80dac-138">Interfaces for the DMO</span></span>

<span data-ttu-id="80dac-139">Если вы создаете в виде DMO экземпляр видеодекодера MPEG4 Part 2, декодер предоставляет следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="80dac-139">If you create an instance of the MPEG4 Part 2 Video decoder as a DMO, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="80dac-140">**имедиаобжект**</span><span class="sxs-lookup"><span data-stu-id="80dac-140">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="80dac-141">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="80dac-141">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)

<span data-ttu-id="80dac-142">Вы можете получить интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , вызвав **CoCreateInstance**, а также получить интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) путем вызова **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="80dac-142">You can obtain an [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface by calling **CoCreateInstance**, and you can obtain an [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface by calling **QueryInterface**.</span></span>

## <a name="interfaces-for-the-mft"></a><span data-ttu-id="80dac-143">Интерфейсы для MFT</span><span class="sxs-lookup"><span data-stu-id="80dac-143">Interfaces for the MFT</span></span>

<span data-ttu-id="80dac-144">Если вы создаете в MFT экземпляр видеодекодера MPEG2 Part 2, декодер предоставляет следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="80dac-144">If you create an instance of the MPEG2 Part 2 Video decoder as an MFT, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="80dac-145">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="80dac-145">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="80dac-146">**имфаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="80dac-146">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="80dac-147">**имфкуалитядвисе**</span><span class="sxs-lookup"><span data-stu-id="80dac-147">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="80dac-148">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="80dac-148">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="80dac-149">**имфратеконтрол**</span><span class="sxs-lookup"><span data-stu-id="80dac-149">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="80dac-150">**имфратесуппорт**</span><span class="sxs-lookup"><span data-stu-id="80dac-150">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

<span data-ttu-id="80dac-151">Можно получить указатель на интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , вызвав **CoCreateInstance**, и можно получить указатель на интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , вызвав [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span><span class="sxs-lookup"><span data-stu-id="80dac-151">You can obtain a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface by calling **CoCreateInstance**, and you can obtain a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface by calling [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span></span> <span data-ttu-id="80dac-152">Указатель на интерфейс [**имфкуалитядвисе**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) или [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) можно получить, вызвав **QueryInterface** в MFT.</span><span class="sxs-lookup"><span data-stu-id="80dac-152">You can obtain a pointer to the [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) or [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) interface by calling **QueryInterface** on the MFT.</span></span> <span data-ttu-id="80dac-153">Вы можете получить указатель на интерфейс [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) или [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , вызвав [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) и передав **\_ \_ \_ службе управления тарифным курсом** Service идентификатор MF.</span><span class="sxs-lookup"><span data-stu-id="80dac-153">You can obtain a pointer to the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) or [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and passing the service identifier **MF\_RATE\_CONTROL\_SERVICE**.</span></span>

## <a name="profiles-and-levels"></a><span data-ttu-id="80dac-154">Профили и уровни</span><span class="sxs-lookup"><span data-stu-id="80dac-154">Profiles and Levels</span></span>

<span data-ttu-id="80dac-155">Спецификация MPEG4 определяет несколько профилей, каждый из которых задает инструменты, которые кодировщик может использовать для создания закодированного потока.</span><span class="sxs-lookup"><span data-stu-id="80dac-155">The MPEG4 specification defines several profiles, each of which specifies the tools that an encoder can use to generate an encoded stream.</span></span> <span data-ttu-id="80dac-156">Декодер видео MPEG4 M89 поддерживает два профиля: простой визуальный профиль и расширенный простой профиль.</span><span class="sxs-lookup"><span data-stu-id="80dac-156">The MPEG4 Part2 Video Decoder supports two of those profiles: Simple Visual Profile and Advanced Simple Profile.</span></span> <span data-ttu-id="80dac-157">Иными словами, видеодекодер MPEG4 Part 2 может декодировать потоки, закодированные в соответствии с простым визуальным профилем или расширенным простым профилем.</span><span class="sxs-lookup"><span data-stu-id="80dac-157">In other words, the MPEG4 Part 2 Video decoder can decode streams that were encoded according to either the Simple Visual Profile or the Advanced Simple Profile.</span></span>

<span data-ttu-id="80dac-158">Простой визуальный профиль поддерживает базовую передачу видео с низкой скоростью передачи данных в прогрессивном режиме.</span><span class="sxs-lookup"><span data-stu-id="80dac-158">The Simple Visual Profile supports basic transmission of low bit-rate video in progressive mode.</span></span> <span data-ttu-id="80dac-159">Он поддерживает только рисунки внутри и прогноза.</span><span class="sxs-lookup"><span data-stu-id="80dac-159">It supports only Intra and Prediction pictures.</span></span> <span data-ttu-id="80dac-160">Он также поддерживает короткий режим заголовков, который обратно совместим с базовым профилем H. 263.</span><span class="sxs-lookup"><span data-stu-id="80dac-160">It also supports the short header mode, which is backward compatible with the H.263 baseline profile.</span></span> <span data-ttu-id="80dac-161">Начиная с Windows 10 видеодекодер MPEG-4 Part 2 также поддерживает H. 263v2 (H. 263 +), который поддерживает пользовательские размеры изображений.</span><span class="sxs-lookup"><span data-stu-id="80dac-161">Starting with Windows 10, the MPEG-4 Part 2 Video Decoder also supports H.263v2 (H.263+) which supports custom picture sizes.</span></span>

<span data-ttu-id="80dac-162">Расширенный простой профиль поддерживает все средства простого визуального профиля, а также поддерживает чередование видео, B-кадров, квартальной компенсации движения в PEL, дополнительные дискретизация таблицы и глобальную компенсацию движения.</span><span class="sxs-lookup"><span data-stu-id="80dac-162">The Advanced Simple Profile supports all the tools of the Simple Visual Profile and, in addition, supports interlaced video, B-frames, quarter-pel motion compensation, additional quantization tables, and global motion compensation.</span></span>

<span data-ttu-id="80dac-163">Спецификация MPEG4 также определяет несколько уровней, каждый из которых задает ограничения для выходного потока, созданного кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="80dac-163">The MPEG4 specification also defines several levels, each of which specifies constraints on the output stream generated by an encoder.</span></span>

<span data-ttu-id="80dac-164">В следующей таблице показаны профили и уровни, а также типичные разрешения, поддерживаемые видеодекодером MPEG4 Part 2.</span><span class="sxs-lookup"><span data-stu-id="80dac-164">The following table shows the profiles and levels, along with typical resolutions, supported by the MPEG4 Part 2 Video decoder.</span></span>



| <span data-ttu-id="80dac-165">Профиль</span><span class="sxs-lookup"><span data-stu-id="80dac-165">Profile</span></span>         | <span data-ttu-id="80dac-166">Level</span><span class="sxs-lookup"><span data-stu-id="80dac-166">Level</span></span> | <span data-ttu-id="80dac-167">Типичное разрешение</span><span class="sxs-lookup"><span data-stu-id="80dac-167">Typical Resolution</span></span> |
|-----------------|-------|--------------------|
| <span data-ttu-id="80dac-168">Простой визуальный элемент</span><span class="sxs-lookup"><span data-stu-id="80dac-168">Simple Visual</span></span>   | <span data-ttu-id="80dac-169">0</span><span class="sxs-lookup"><span data-stu-id="80dac-169">0</span></span>     | <span data-ttu-id="80dac-170">176 x 144</span><span class="sxs-lookup"><span data-stu-id="80dac-170">176 x 144</span></span>          |
| <span data-ttu-id="80dac-171">Простой визуальный элемент</span><span class="sxs-lookup"><span data-stu-id="80dac-171">Simple Visual</span></span>   | <span data-ttu-id="80dac-172">1</span><span class="sxs-lookup"><span data-stu-id="80dac-172">1</span></span>     | <span data-ttu-id="80dac-173">176 x 144</span><span class="sxs-lookup"><span data-stu-id="80dac-173">176 x 144</span></span>          |
| <span data-ttu-id="80dac-174">Простой визуальный элемент</span><span class="sxs-lookup"><span data-stu-id="80dac-174">Simple Visual</span></span>   | <span data-ttu-id="80dac-175">2</span><span class="sxs-lookup"><span data-stu-id="80dac-175">2</span></span>     | <span data-ttu-id="80dac-176">352 x 288</span><span class="sxs-lookup"><span data-stu-id="80dac-176">352 x 288</span></span>          |
| <span data-ttu-id="80dac-177">Простой визуальный элемент</span><span class="sxs-lookup"><span data-stu-id="80dac-177">Simple Visual</span></span>   | <span data-ttu-id="80dac-178">3</span><span class="sxs-lookup"><span data-stu-id="80dac-178">3</span></span>     | <span data-ttu-id="80dac-179">352 x 288</span><span class="sxs-lookup"><span data-stu-id="80dac-179">352 x 288</span></span>          |
| <span data-ttu-id="80dac-180">симплевисуал</span><span class="sxs-lookup"><span data-stu-id="80dac-180">SimpleVisual</span></span>    | <span data-ttu-id="80dac-181">4a</span><span class="sxs-lookup"><span data-stu-id="80dac-181">4a</span></span>    | <span data-ttu-id="80dac-182">640 x 480</span><span class="sxs-lookup"><span data-stu-id="80dac-182">640 x 480</span></span>          |
| <span data-ttu-id="80dac-183">Простой визуальный элемент</span><span class="sxs-lookup"><span data-stu-id="80dac-183">Simple Visual</span></span>   | <span data-ttu-id="80dac-184">5</span><span class="sxs-lookup"><span data-stu-id="80dac-184">5</span></span>     | <span data-ttu-id="80dac-185">720 x 576</span><span class="sxs-lookup"><span data-stu-id="80dac-185">720 x 576</span></span>          |
| <span data-ttu-id="80dac-186">Расширенный простой</span><span class="sxs-lookup"><span data-stu-id="80dac-186">Advanced Simple</span></span> | <span data-ttu-id="80dac-187">0</span><span class="sxs-lookup"><span data-stu-id="80dac-187">0</span></span>     | <span data-ttu-id="80dac-188">176 x 144</span><span class="sxs-lookup"><span data-stu-id="80dac-188">176 x 144</span></span>          |
| <span data-ttu-id="80dac-189">Расширенный простой</span><span class="sxs-lookup"><span data-stu-id="80dac-189">Advanced Simple</span></span> | <span data-ttu-id="80dac-190">1</span><span class="sxs-lookup"><span data-stu-id="80dac-190">1</span></span>     | <span data-ttu-id="80dac-191">176 x 144</span><span class="sxs-lookup"><span data-stu-id="80dac-191">176 x 144</span></span>          |
| <span data-ttu-id="80dac-192">Расширенный простой</span><span class="sxs-lookup"><span data-stu-id="80dac-192">Advanced Simple</span></span> | <span data-ttu-id="80dac-193">2</span><span class="sxs-lookup"><span data-stu-id="80dac-193">2</span></span>     | <span data-ttu-id="80dac-194">352 x 288</span><span class="sxs-lookup"><span data-stu-id="80dac-194">352 x 288</span></span>          |
| <span data-ttu-id="80dac-195">Расширенный простой</span><span class="sxs-lookup"><span data-stu-id="80dac-195">Advanced Simple</span></span> | <span data-ttu-id="80dac-196">3</span><span class="sxs-lookup"><span data-stu-id="80dac-196">3</span></span>     | <span data-ttu-id="80dac-197">352 x 288</span><span class="sxs-lookup"><span data-stu-id="80dac-197">352 x 288</span></span>          |
| <span data-ttu-id="80dac-198">Расширенный простой</span><span class="sxs-lookup"><span data-stu-id="80dac-198">Advanced Simple</span></span> | <span data-ttu-id="80dac-199">3б</span><span class="sxs-lookup"><span data-stu-id="80dac-199">3b</span></span>    | <span data-ttu-id="80dac-200">352 x 288</span><span class="sxs-lookup"><span data-stu-id="80dac-200">352 x 288</span></span>          |
| <span data-ttu-id="80dac-201">Расширенный простой</span><span class="sxs-lookup"><span data-stu-id="80dac-201">Advanced Simple</span></span> | <span data-ttu-id="80dac-202">4</span><span class="sxs-lookup"><span data-stu-id="80dac-202">4</span></span>     | <span data-ttu-id="80dac-203">352 x 756</span><span class="sxs-lookup"><span data-stu-id="80dac-203">352 x 756</span></span>          |
| <span data-ttu-id="80dac-204">Расширенный простой</span><span class="sxs-lookup"><span data-stu-id="80dac-204">Advanced Simple</span></span> | <span data-ttu-id="80dac-205">5</span><span class="sxs-lookup"><span data-stu-id="80dac-205">5</span></span>     | <span data-ttu-id="80dac-206">720 x 576</span><span class="sxs-lookup"><span data-stu-id="80dac-206">720 x 576</span></span>          |



 

<span data-ttu-id="80dac-207">Дополнительные сведения о профилях и уровнях см. в спецификации MPEG4 Part 2 (ISO/IEC 14496-2): информационные технологии — Программирование звуковых визуальных объектов — часть 2: Visual.</span><span class="sxs-lookup"><span data-stu-id="80dac-207">For more information about profiles and levels, see the MPEG4 Part 2 specification (ISO/IEC 14496-2): Information technology -- Coding of audio-visual objects -- Part 2: Visual.</span></span>

## <a name="decoder-properties"></a><span data-ttu-id="80dac-208">Свойства декодера</span><span class="sxs-lookup"><span data-stu-id="80dac-208">Decoder Properties</span></span>

<span data-ttu-id="80dac-209">Чтобы задать свойства видеодекодера 1 части MPEG4, используйте интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) или интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="80dac-209">To set properties on the MPEG4 Part 2 Video decoder, use the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface or the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="80dac-210">Видеодекодер MPEG4 Part 2 поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="80dac-210">The MPEG4 Part 2 Video decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="80dac-211">Свойство</span><span class="sxs-lookup"><span data-stu-id="80dac-211">Property</span></span></th>
<th><span data-ttu-id="80dac-212">Описание</span><span class="sxs-lookup"><span data-stu-id="80dac-212">Description</span></span></th>
<th><span data-ttu-id="80dac-213">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="80dac-213">Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="80dac-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span><span class="sxs-lookup"><span data-stu-id="80dac-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span></span></td>
<td><span data-ttu-id="80dac-215">Задает уровень питания.</span><span class="sxs-lookup"><span data-stu-id="80dac-215">Specifies the power level.</span></span><br/> <dl> <span data-ttu-id="80dac-216">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="80dac-216">Windows 7.</span></span><br />
<span data-ttu-id="80dac-217">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="80dac-217">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="80dac-218">100</span><span class="sxs-lookup"><span data-stu-id="80dac-218">100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80dac-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="80dac-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span></span></td>
<td><span data-ttu-id="80dac-220">Задает режим формирования эскиза.</span><span class="sxs-lookup"><span data-stu-id="80dac-220">Specifies the thumbnail generation mode.</span></span><br/> <dl> <span data-ttu-id="80dac-221">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="80dac-221">Windows 7.</span></span><br />
<span data-ttu-id="80dac-222">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="80dac-222">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="80dac-223"><strong>VARIANT_FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="80dac-223"><strong>VARIANT_FALSE</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="80dac-224">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80dac-224">Remarks</span></span>

<span data-ttu-id="80dac-225">Глобальные уникальные идентификаторы (GUID) для подтипов мультимедиа RGB различаются в зависимости от того, выступает ли декодер в качестве DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="80dac-225">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="80dac-226">Идентификаторы GUID для подтипов мультимедиа, отличных от RGB, одинаковы, независимо от того, выступает ли декодер в качестве DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="80dac-226">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="80dac-227">Сведения об идентификаторах GUID, представляющих подтипы мультимедиа, см. в разделе [типы носителей](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="80dac-227">For information about the GUIDs that represent media subtypes, see [Media Types](media-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80dac-228">Требования</span><span class="sxs-lookup"><span data-stu-id="80dac-228">Requirements</span></span>



| <span data-ttu-id="80dac-229">Требование</span><span class="sxs-lookup"><span data-stu-id="80dac-229">Requirement</span></span> | <span data-ttu-id="80dac-230">Значение</span><span class="sxs-lookup"><span data-stu-id="80dac-230">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80dac-231">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80dac-231">Minimum supported client</span></span><br/> | <span data-ttu-id="80dac-232">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="80dac-232">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="80dac-233">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80dac-233">Minimum supported server</span></span><br/> | <span data-ttu-id="80dac-234">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="80dac-234">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="80dac-235">Header</span><span class="sxs-lookup"><span data-stu-id="80dac-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="80dac-236"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="80dac-236"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="80dac-237">DLL</span><span class="sxs-lookup"><span data-stu-id="80dac-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80dac-238"><dt>MP4SDecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80dac-238"><dt>MP4SDecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80dac-239">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80dac-239">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80dac-240">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="80dac-240">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
