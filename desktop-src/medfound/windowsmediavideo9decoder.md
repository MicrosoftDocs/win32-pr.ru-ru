---
description: Декодер видео Windows Media 9 декодирует видеопотоки, закодированные кодировщиком Windows Media Video.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Декодер Windows Media Video 9 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718023"
---
# <a name="windows-media-video-9-decoder"></a><span data-ttu-id="f8126-103">Декодер Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="f8126-103">Windows Media Video 9 Decoder</span></span>

<span data-ttu-id="f8126-104">Декодер видео Windows Media 9 декодирует видеопотоки, закодированные [**кодировщиком Windows Media Video**](windowsmediavideo9encoder.md).</span><span class="sxs-lookup"><span data-stu-id="f8126-104">The Windows Media Video 9 decoder decodes video streams that were encoded by the [**Windows Media Video Encoder**](windowsmediavideo9encoder.md).</span></span> <span data-ttu-id="f8126-105">Кодировщик и декодер поддерживают следующие четыре категории закодированного видео.</span><span class="sxs-lookup"><span data-stu-id="f8126-105">The encoder and decoder support the following four categories of encoded video.</span></span>

-   <span data-ttu-id="f8126-106">Простой профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="f8126-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="f8126-107">Основной профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="f8126-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="f8126-108">Расширенный профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="f8126-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="f8126-109">Изображение Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="f8126-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="f8126-110">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="f8126-110">Class Identifier</span></span>

<span data-ttu-id="f8126-111">Идентификатор класса (CLSID) для видеодекодера Windows Media представлен константой **CLSID \_ квмвдекмедиаобжект**.</span><span class="sxs-lookup"><span data-stu-id="f8126-111">The class identifier (CLSID) for the Windows Media Video decoder is represented by the constant **CLSID\_CWMVDecMediaObject**.</span></span> <span data-ttu-id="f8126-112">Вы можете создать экземпляр видеодекодера, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="f8126-112">You can create an instance of the video decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="f8126-113">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="f8126-113">Interfaces</span></span>

<span data-ttu-id="f8126-114">Объект видеодекодера предоставляет интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="f8126-114">A video decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="f8126-115">Видеодекодер ведет себя как DMO или файл MFT в зависимости от того, какие интерфейсы вы получаете и какая версия Windows выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8126-115">A video decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="f8126-116">В следующей таблице показаны условия, при которых декодер видео ведет себя как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="f8126-116">The following table shows the conditions under which a video decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="f8126-117">Операционная система</span><span class="sxs-lookup"><span data-stu-id="f8126-117">Operating system</span></span>            | <span data-ttu-id="f8126-118">Поведение декодера</span><span class="sxs-lookup"><span data-stu-id="f8126-118">Decoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8126-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f8126-119">Windows XP</span></span>                  | <span data-ttu-id="f8126-120">Видеодекодер Windows Media всегда ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="f8126-120">A Windows Media video decoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="f8126-121">Windows Vista и Windows 7</span><span class="sxs-lookup"><span data-stu-id="f8126-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="f8126-122">По умолчанию видеодекодер Windows Media ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="f8126-122">By default, a Windows Media video decoder behaves as a DMO.</span></span> <span data-ttu-id="f8126-123">Если вы получаете интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) для видеодекодера, он ведет себя как файл MFT.</span><span class="sxs-lookup"><span data-stu-id="f8126-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="f8126-124">Начиная с Windows 7, декодер видео Windows Media реализует интерфейс [**идмокуалитиконтрол**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .</span><span class="sxs-lookup"><span data-stu-id="f8126-124">Beginning with Windows 7, the Windows Media Video decoder implements the [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) interface.</span></span>

## <a name="input-formats"></a><span data-ttu-id="f8126-125">Форматы входных данных</span><span class="sxs-lookup"><span data-stu-id="f8126-125">Input Formats</span></span>

<span data-ttu-id="f8126-126">В следующей таблице показаны 4-символьные коды (Фаурккс), соответствующие категориям закодированных входных данных, поддерживаемых декодером Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="f8126-126">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded input that are supported by the Windows Media Video decoder.</span></span>



| <span data-ttu-id="f8126-127">Категория</span><span class="sxs-lookup"><span data-stu-id="f8126-127">Category</span></span>                               | <span data-ttu-id="f8126-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="f8126-128">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="f8126-129">Простой профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="f8126-129">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="f8126-130">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="f8126-130">"WMV3"</span></span>                                   |
| <span data-ttu-id="f8126-131">Основной профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="f8126-131">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="f8126-132">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="f8126-132">"WMV3"</span></span>                                   |
| <span data-ttu-id="f8126-133">Расширенный профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="f8126-133">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="f8126-134">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="f8126-134">"WVC1"</span></span>                                   |
| <span data-ttu-id="f8126-135">Изображение Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="f8126-135">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="f8126-136">"ВМВП" для 9,1, "WVP2" для 9,1 версии 2</span><span class="sxs-lookup"><span data-stu-id="f8126-136">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="f8126-137">Форматы выходных данных</span><span class="sxs-lookup"><span data-stu-id="f8126-137">Output Formats</span></span>

<span data-ttu-id="f8126-138">Декодер видео Windows Media поддерживает следующие подтипы выходных данных, когда он выступает в роли DMO.</span><span class="sxs-lookup"><span data-stu-id="f8126-138">The Windows Media Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="f8126-139">МЕДИАСУБТИПЕ \_ NV12</span><span class="sxs-lookup"><span data-stu-id="f8126-139">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="f8126-140">МЕДИАСУБТИПЕ \_ YV12</span><span class="sxs-lookup"><span data-stu-id="f8126-140">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="f8126-141">МЕДИАСУБТИПЕ \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="f8126-141">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="f8126-142">МЕДИАСУБТИПЕ \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="f8126-142">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="f8126-143">МЕДИАСУБТИПЕ \_ ивю</span><span class="sxs-lookup"><span data-stu-id="f8126-143">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="f8126-144">МЕДИАСУБТИПЕ \_ NV11</span><span class="sxs-lookup"><span data-stu-id="f8126-144">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="f8126-145">МЕДИАСУБТИПЕ \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="f8126-145">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="f8126-146">МЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="f8126-146">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="f8126-147">МЕДИАСУБТИПЕ \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="f8126-147">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="f8126-148">МЕДИАСУБТИПЕ \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="f8126-148">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="f8126-149">МЕДИАСУБТИПЕ \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="f8126-149">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="f8126-150">Декодер видео Windows Media поддерживает следующие подтипы выходных данных, когда он выступает в качестве MFT.</span><span class="sxs-lookup"><span data-stu-id="f8126-150">The Windows Media Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="f8126-151">Мфвидеоформат \_ NV12</span><span class="sxs-lookup"><span data-stu-id="f8126-151">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="f8126-152">Мфвидеоформат \_ YV12</span><span class="sxs-lookup"><span data-stu-id="f8126-152">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="f8126-153">Мфвидеоформат \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="f8126-153">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="f8126-154">Мфвидеоформат \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="f8126-154">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="f8126-155">Мфвидеоформат \_ ивю</span><span class="sxs-lookup"><span data-stu-id="f8126-155">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="f8126-156">Мфвидеоформат \_ NV11</span><span class="sxs-lookup"><span data-stu-id="f8126-156">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="f8126-157">Мфвидеоформат \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="f8126-157">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="f8126-158">Мфвидеоформат \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="f8126-158">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="f8126-159">Мфвидеоформат \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="f8126-159">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="f8126-160">Мфвидеоформат \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="f8126-160">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="f8126-161">Мфвидеоформат \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="f8126-161">MFVideoFormat\_RGB8</span></span>

## <a name="properties"></a><span data-ttu-id="f8126-162">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8126-162">Properties</span></span>

<span data-ttu-id="f8126-163">Декодер видео Windows Media поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f8126-163">The Windows Media Video decoder supports the following properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8126-164">Свойство</span><span class="sxs-lookup"><span data-stu-id="f8126-164">Property</span></span></th>
<th><span data-ttu-id="f8126-165">Описание</span><span class="sxs-lookup"><span data-stu-id="f8126-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f8126-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span><span class="sxs-lookup"><span data-stu-id="f8126-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span></span></td>
<td><span data-ttu-id="f8126-167">Указывает, будет ли кодек декодировать чередующиеся видеокадры из сжатого потока в виде прогрессивных кадров.</span><span class="sxs-lookup"><span data-stu-id="f8126-167">Specifies whether the codec decodes interlaced video frames from the compressed stream as progressive frames.</span></span><br/> <dl> <span data-ttu-id="f8126-168">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="f8126-168">Windows XP and later.</span></span><br />
<span data-ttu-id="f8126-169">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="f8126-169">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="f8126-170">Read/write.</span><span class="sxs-lookup"><span data-stu-id="f8126-170">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8126-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="f8126-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span></span></td>
<td><span data-ttu-id="f8126-172">Указывает, будет ли декодер использовать аппаратное ускорение DirectX Video, если оно доступно.</span><span class="sxs-lookup"><span data-stu-id="f8126-172">Specifies whether the decoder will use DirectX video acceleration hardware, if available.</span></span><br/> <dl> <span data-ttu-id="f8126-173">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="f8126-173">Windows XP and later.</span></span><br />
<span data-ttu-id="f8126-174">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="f8126-174">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="f8126-175">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="f8126-175">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8126-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span><span class="sxs-lookup"><span data-stu-id="f8126-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span></span></td>
<td><span data-ttu-id="f8126-177">Задает уровень питания для декодера.</span><span class="sxs-lookup"><span data-stu-id="f8126-177">Specifies the power level for the decoder.</span></span><br/> <dl> <span data-ttu-id="f8126-178">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f8126-178">Windows 7.</span></span><br />
<span data-ttu-id="f8126-179">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="f8126-179">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="f8126-180">Read/write.</span><span class="sxs-lookup"><span data-stu-id="f8126-180">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8126-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="f8126-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span></span></td>
<td><span data-ttu-id="f8126-182">Указывает, следует ли декодеру использовать интерполяцию кадров.</span><span class="sxs-lookup"><span data-stu-id="f8126-182">Specifies whether the decoder should use frame interpolation.</span></span><br/> <dl> <span data-ttu-id="f8126-183">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="f8126-183">Windows XP and later.</span></span><br />
<span data-ttu-id="f8126-184">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="f8126-184">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="f8126-185">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="f8126-185">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8126-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span><span class="sxs-lookup"><span data-stu-id="f8126-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span></span></td>
<td><span data-ttu-id="f8126-187">Указывает, поддерживает ли декодер интерполяцию кадров.</span><span class="sxs-lookup"><span data-stu-id="f8126-187">Specifies whether the decoder supports frame interpolation.</span></span><br/> <dl> <span data-ttu-id="f8126-188">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="f8126-188">Windows XP and later.</span></span><br />
<span data-ttu-id="f8126-189">Простой профиль, основной профиль, расширенный профиль, изображение</span><span class="sxs-lookup"><span data-stu-id="f8126-189">Simple Profile, Main Profile, Advanced Profile, Image</span></span><br />
<span data-ttu-id="f8126-190">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f8126-190">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8126-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span><span class="sxs-lookup"><span data-stu-id="f8126-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span></span></td>
<td><span data-ttu-id="f8126-192">Указывает число потоков, которые будет использовать декодер.</span><span class="sxs-lookup"><span data-stu-id="f8126-192">Specifies the number of threads that the decoder will use.</span></span><br/> <dl> <span data-ttu-id="f8126-193">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="f8126-193">Windows Vista and later.</span></span><br />
<span data-ttu-id="f8126-194">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="f8126-194">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="f8126-195">Read/write.</span><span class="sxs-lookup"><span data-stu-id="f8126-195">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8126-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span><span class="sxs-lookup"><span data-stu-id="f8126-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span></span></td>
<td><span data-ttu-id="f8126-197">Задает режим обработки, выполняемый для декодера.</span><span class="sxs-lookup"><span data-stu-id="f8126-197">Specifies the post processing mode for the decoder.</span></span><br/> <dl> <span data-ttu-id="f8126-198">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="f8126-198">Windows Vista and later.</span></span><br />
<span data-ttu-id="f8126-199">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="f8126-199">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="f8126-200">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="f8126-200">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8126-201"><strong>g_wszWMVCNeedsDrain</strong></span><span class="sxs-lookup"><span data-stu-id="f8126-201"><strong>g_wszWMVCNeedsDrain</strong></span></span></td>
<td><span data-ttu-id="f8126-202">Указывает, следует ли сливировать декодер.</span><span class="sxs-lookup"><span data-stu-id="f8126-202">Specifies whether the decoder should be drained.</span></span><br/> <dl> <span data-ttu-id="f8126-203">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f8126-203">Windows 8</span></span><br />
<span data-ttu-id="f8126-204">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f8126-204">Read-only.</span></span><br />
</dl> <span data-ttu-id="f8126-205">Это свойство используется средой выполнения формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f8126-205">This property is used by the Windows Media Format runtime.</span></span> <span data-ttu-id="f8126-206">Тип свойства — <strong>VARIANT_BOOL</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8126-206">The property type is <strong>VARIANT_BOOL</strong>.</span></span> <span data-ttu-id="f8126-207">Если значение равно <strong>VARIANT_TRUE</strong>, декодер должен быть остановлен после небесперебойности.</span><span class="sxs-lookup"><span data-stu-id="f8126-207">If the value is <strong>VARIANT_TRUE</strong>, the decoder should be drained after a discontinuity.</span></span> <span data-ttu-id="f8126-208">Дополнительные сведения о стоке MFT см. в разделе <a href="basic-mft-processing-model.md">Базовая модель обработки MFT</a>.</span><span class="sxs-lookup"><span data-stu-id="f8126-208">For more information about draining an MFT, see <a href="basic-mft-processing-model.md">Basic MFT Processing Model</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f8126-209">Чтобы запросить это свойство, используйте интерфейс <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>ипропертибаг</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f8126-209">To query this property, use the <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> interface.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f8126-210">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8126-210">Remarks</span></span>

<span data-ttu-id="f8126-211">Максимально допустимое разрешение декодера Windows Media Video 9 — 4096x4096.</span><span class="sxs-lookup"><span data-stu-id="f8126-211">The maximum resolution allowed by the Windows Media Video 9 decoder is 4096x4096.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8126-212">Требования</span><span class="sxs-lookup"><span data-stu-id="f8126-212">Requirements</span></span>



| <span data-ttu-id="f8126-213">Требование</span><span class="sxs-lookup"><span data-stu-id="f8126-213">Requirement</span></span> | <span data-ttu-id="f8126-214">Значение</span><span class="sxs-lookup"><span data-stu-id="f8126-214">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8126-215">Клиент</span><span class="sxs-lookup"><span data-stu-id="f8126-215">Client</span></span><br/> | <span data-ttu-id="f8126-216">Windows XP, Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="f8126-216">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="f8126-217">Header</span><span class="sxs-lookup"><span data-stu-id="f8126-217">Header</span></span><br/> | <dl> <span data-ttu-id="f8126-218"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8126-218"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="f8126-219">DLL</span><span class="sxs-lookup"><span data-stu-id="f8126-219">DLL</span></span><br/>    | <dl> <span data-ttu-id="f8126-220"><dt>Wmvdecod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8126-220"><dt>Wmvdecod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8126-221">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8126-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8126-222">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="f8126-222">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="f8126-223">Реализация кодека</span><span class="sxs-lookup"><span data-stu-id="f8126-223">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
