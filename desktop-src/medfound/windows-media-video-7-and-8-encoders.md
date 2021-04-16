---
description: Кодировщик Windows Media Video 7/8 реализует предыдущие версии кодировщика видео Windows Media.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Кодировщик Windows Media Video 7/8 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699134"
---
# <a name="windows-media-video-78-encoder"></a><span data-ttu-id="1e81f-103">Кодировщик Windows Media Video 7/8</span><span class="sxs-lookup"><span data-stu-id="1e81f-103">Windows Media Video 7/8 Encoder</span></span>

<span data-ttu-id="1e81f-104">Кодировщик Windows Media Video 7/8 реализует предыдущие версии кодировщика видео Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1e81f-104">The Windows Media Video 7/8 encoder implements previous versions of the Windows Media Video encoder.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="1e81f-105">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="1e81f-105">Class Identifier</span></span>

<span data-ttu-id="1e81f-106">Идентификатор класса (CLSID) для кодировщика Windows Media Video 7/8 — это **CLSID \_ квмвксенкмедиаобжект**.</span><span class="sxs-lookup"><span data-stu-id="1e81f-106">The class identifier (CLSID) for the Windows Media Video 7/8 encoder is **CLSID\_CWMVXEncMediaObject**.</span></span> <span data-ttu-id="1e81f-107">Экземпляр кодировщика можно создать, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="1e81f-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="1e81f-108">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="1e81f-108">Interfaces</span></span>

<span data-ttu-id="1e81f-109">Объект видеокодировщика предоставляет интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="1e81f-109">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="1e81f-110">Видеокодировщик ведет себя как DMO или файл MFT в зависимости от того, какие интерфейсы вы получаете и какая версия Windows выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e81f-110">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="1e81f-111">В следующей таблице показаны условия, при которых кодировщик видео ведет себя как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="1e81f-111">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="1e81f-112">Операционная система</span><span class="sxs-lookup"><span data-stu-id="1e81f-112">Operating system</span></span>            | <span data-ttu-id="1e81f-113">Поведение кодировщика</span><span class="sxs-lookup"><span data-stu-id="1e81f-113">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e81f-114">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e81f-114">Windows XP</span></span>                  | <span data-ttu-id="1e81f-115">Кодировщик Windows Media Video всегда ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="1e81f-115">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="1e81f-116">Windows Vista и Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e81f-116">Windows Vista and Windows 7</span></span> | <span data-ttu-id="1e81f-117">По умолчанию кодировщик видео Windows Media ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="1e81f-117">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="1e81f-118">Если вы получаете интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) для видеокодировщика, он ведет себя как файл MFT.</span><span class="sxs-lookup"><span data-stu-id="1e81f-118">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="1e81f-119">Форматы входных данных</span><span class="sxs-lookup"><span data-stu-id="1e81f-119">Input Formats</span></span>

<span data-ttu-id="1e81f-120">Кодировщик Windows Media Video поддерживает следующие входные подтипы носителей, когда он выступает в роли DMO.</span><span class="sxs-lookup"><span data-stu-id="1e81f-120">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="1e81f-121">МЕДИАСУБТИПЕ \_ ийув</span><span class="sxs-lookup"><span data-stu-id="1e81f-121">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="1e81f-122">МЕДИАСУБТИПЕ \_ I420</span><span class="sxs-lookup"><span data-stu-id="1e81f-122">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="1e81f-123">МЕДИАСУБТИПЕ \_ YV12</span><span class="sxs-lookup"><span data-stu-id="1e81f-123">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="1e81f-124">МЕДИАСУБТИПЕ \_ NV11</span><span class="sxs-lookup"><span data-stu-id="1e81f-124">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="1e81f-125">МЕДИАСУБТИПЕ \_ NV12</span><span class="sxs-lookup"><span data-stu-id="1e81f-125">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="1e81f-126">МЕДИАСУБТИПЕ \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="1e81f-126">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="1e81f-127">МЕДИАСУБТИПЕ \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="1e81f-127">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="1e81f-128">МЕДИАСУБТИПЕ \_ ивю</span><span class="sxs-lookup"><span data-stu-id="1e81f-128">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="1e81f-129">МЕДИАСУБТИПЕ \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="1e81f-129">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="1e81f-130">МЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="1e81f-130">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="1e81f-131">МЕДИАСУБТИПЕ \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="1e81f-131">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="1e81f-132">МЕДИАСУБТИПЕ \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="1e81f-132">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="1e81f-133">МЕДИАСУБТИПЕ \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="1e81f-133">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="1e81f-134">МЕДИАСУБТИПЕ \_</span><span class="sxs-lookup"><span data-stu-id="1e81f-134">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="1e81f-135">Кодировщик Windows Media Video поддерживает следующие входные подтипы носителя, когда он выступает в качестве MFT.</span><span class="sxs-lookup"><span data-stu-id="1e81f-135">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="1e81f-136">Мфвидеоформат \_ ийув</span><span class="sxs-lookup"><span data-stu-id="1e81f-136">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="1e81f-137">Мфвидеоформат \_ I420</span><span class="sxs-lookup"><span data-stu-id="1e81f-137">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="1e81f-138">Мфвидеоформат \_ YV12</span><span class="sxs-lookup"><span data-stu-id="1e81f-138">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="1e81f-139">Мфвидеоформат \_ NV11</span><span class="sxs-lookup"><span data-stu-id="1e81f-139">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="1e81f-140">Мфвидеоформат \_ NV12</span><span class="sxs-lookup"><span data-stu-id="1e81f-140">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="1e81f-141">Мфвидеоформат \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="1e81f-141">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="1e81f-142">Мфвидеоформат \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="1e81f-142">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="1e81f-143">Мфвидеоформат \_ ивю</span><span class="sxs-lookup"><span data-stu-id="1e81f-143">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="1e81f-144">Мфвидеоформат \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="1e81f-144">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="1e81f-145">Мфвидеоформат \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="1e81f-145">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="1e81f-146">Мфвидеоформат \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="1e81f-146">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="1e81f-147">Мфвидеоформат \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="1e81f-147">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="1e81f-148">Мфвидеоформат \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="1e81f-148">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="1e81f-149">МЕДИАСУБТИПЕ \_</span><span class="sxs-lookup"><span data-stu-id="1e81f-149">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="1e81f-150">Форматы выходных данных</span><span class="sxs-lookup"><span data-stu-id="1e81f-150">Output Formats</span></span>

<span data-ttu-id="1e81f-151">В следующей таблице показаны коды из четырех символов (Фаурккс) для типов выходных данных, поддерживаемых кодировщиком Windows Media Video 7/8.</span><span class="sxs-lookup"><span data-stu-id="1e81f-151">The following table shows the four-character codes (FOURCCs) for the output types supported by the Windows Media Video 7/8 encoder.</span></span>



| <span data-ttu-id="1e81f-152">Категория</span><span class="sxs-lookup"><span data-stu-id="1e81f-152">Category</span></span>              | <span data-ttu-id="1e81f-153">FOURCC</span><span class="sxs-lookup"><span data-stu-id="1e81f-153">FOURCC</span></span> |
|-----------------------|--------|
| <span data-ttu-id="1e81f-154">Windows Media Video 7</span><span class="sxs-lookup"><span data-stu-id="1e81f-154">Windows Media Video 7</span></span> | <span data-ttu-id="1e81f-155">"WMV1"</span><span class="sxs-lookup"><span data-stu-id="1e81f-155">"WMV1"</span></span> |
| <span data-ttu-id="1e81f-156">Windows Media Video 8</span><span class="sxs-lookup"><span data-stu-id="1e81f-156">Windows Media Video 8</span></span> | <span data-ttu-id="1e81f-157">"WMV2"</span><span class="sxs-lookup"><span data-stu-id="1e81f-157">"WMV2"</span></span> |



 

## <a name="properties"></a><span data-ttu-id="1e81f-158">Свойства</span><span class="sxs-lookup"><span data-stu-id="1e81f-158">Properties</span></span>

<span data-ttu-id="1e81f-159">Кодировщик Windows Media Video 7/8 поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1e81f-159">The Windows Media Video 7/8 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1e81f-160">Свойство</span><span class="sxs-lookup"><span data-stu-id="1e81f-160">Property</span></span></th>
<th><span data-ttu-id="1e81f-161">Описание</span><span class="sxs-lookup"><span data-stu-id="1e81f-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e81f-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-163">Указывает дополнительную нагрузку в байтах на пакет, необходимую для контейнера, используемого для хранения сжатого содержимого.</span><span class="sxs-lookup"><span data-stu-id="1e81f-163">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="1e81f-164">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-164">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-165">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-165">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-167">Указывает среднюю частоту кадров содержимого видео в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="1e81f-167">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="1e81f-168">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-168">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-169">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1e81f-169">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-171">Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с средней скоростью (заданным <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="1e81f-171">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="1e81f-172">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-172">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-173">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1e81f-173">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-175">Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с пиковой скоростью (заданное <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="1e81f-175">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="1e81f-176">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-176">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-177">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1e81f-177">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-179">Указывает, содержит ли закодированный поток видео значение полных буферов со всеми ключевыми кадрами.</span><span class="sxs-lookup"><span data-stu-id="1e81f-179">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="1e81f-180">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-180">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-181">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1e81f-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-183">Указывает число кадров видео, закодированных кодеком.</span><span class="sxs-lookup"><span data-stu-id="1e81f-183">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="1e81f-184">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-184">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-185">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1e81f-185">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-187">Указывает количество видеокадров, закодированных кодеком, который фактически содержит данные.</span><span class="sxs-lookup"><span data-stu-id="1e81f-187">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="1e81f-188">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-188">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-189">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1e81f-189">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-191">Это свойство заменяется <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1e81f-191">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-193">Указывает сложность алгоритма кодировщика.</span><span class="sxs-lookup"><span data-stu-id="1e81f-193">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="1e81f-194">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-194">Windows Vista and later.</span></span><br />
<span data-ttu-id="1e81f-195">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-195">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-197">Задает числовое представление компромисса между плавностью движения и качеством изображения в выходных данных кодека.</span><span class="sxs-lookup"><span data-stu-id="1e81f-197">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="1e81f-198">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-198">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-199">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-199">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-201">Указывает шаблон соответствия устройства, которому соответствует закодированное содержимое.</span><span class="sxs-lookup"><span data-stu-id="1e81f-201">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="1e81f-202">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-202">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-203">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1e81f-203">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-205">Указывает шаблон соответствия устройств, который вы хотите использовать для кодирования видео.</span><span class="sxs-lookup"><span data-stu-id="1e81f-205">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="1e81f-206">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-206">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-207">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-207">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-209">Указывает число кадров видео, отброшенных во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="1e81f-209">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="1e81f-210">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-210">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-211">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1e81f-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-213">Задает конец прохода кодирования.</span><span class="sxs-lookup"><span data-stu-id="1e81f-213">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="1e81f-214">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-214">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-215">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-215">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-217">Указывает FOURCC, определяющую кодировщик, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="1e81f-217">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="1e81f-218">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-218">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-219">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-219">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-221">Указывает, следует ли использовать чередование выходных данных кодека.</span><span class="sxs-lookup"><span data-stu-id="1e81f-221">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="1e81f-222">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-222">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-223">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-223">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-225">Указывает максимальное время в миллисекундах между опорными кадрами в выходных коде.</span><span class="sxs-lookup"><span data-stu-id="1e81f-225">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="1e81f-226">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-226">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-227">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-227">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-229">Указывает максимальное число проходов, поддерживаемое кодеком.</span><span class="sxs-lookup"><span data-stu-id="1e81f-229">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="1e81f-230">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-230">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-231">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1e81f-231">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-233">Указывает число проходов, которые кодек будет использовать для кодирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="1e81f-233">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="1e81f-234">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-234">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-235">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1e81f-235">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-237">Указывает, создает ли кодировщик фиктивные записи кадра в битовом потоке для повторяющихся кадров.</span><span class="sxs-lookup"><span data-stu-id="1e81f-237">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="1e81f-238">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-238">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-239">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-239">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-241">Указывает QP.</span><span class="sxs-lookup"><span data-stu-id="1e81f-241">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="1e81f-242">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-242">Windows Vista and later.</span></span><br />
<span data-ttu-id="1e81f-243">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-243">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-245">Указывает среднюю скорость потока в битах в секунду, используемую для 2-проходной кодировки с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="1e81f-245">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="1e81f-246">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-246">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-247">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1e81f-247">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-249">Указывает пиковую скорость потока (в битах в секунду), используемую для ограниченного 2-прохода переменной-разрядной скорости (VBR).</span><span class="sxs-lookup"><span data-stu-id="1e81f-249">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="1e81f-250">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-250">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-251">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1e81f-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-253">Указывает число кадров видео, переданных кодировщику во время процесса кодирования.</span><span class="sxs-lookup"><span data-stu-id="1e81f-253">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="1e81f-254">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-254">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-255">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1e81f-255">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-257">Указывает, будет ли кодек использовать кодирование с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="1e81f-257">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="1e81f-258">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-258">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-259">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1e81f-259">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-261">Задает реальный уровень качества для кодирования с переменной скоростью (1 проход) с учетом качества (с частотой VBR).</span><span class="sxs-lookup"><span data-stu-id="1e81f-261">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="1e81f-262">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-262">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-263">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-263">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e81f-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-265">Указывает объем содержимого в миллисекундах, который может поместиться в буфер модели.</span><span class="sxs-lookup"><span data-stu-id="1e81f-265">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="1e81f-266">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-266">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-267">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1e81f-267">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e81f-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e81f-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1e81f-269">Указывает число пропущенных видеокадров, так как они являлись дубликатами предыдущих кадров.</span><span class="sxs-lookup"><span data-stu-id="1e81f-269">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="1e81f-270">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1e81f-270">Windows XP and later.</span></span><br />
<span data-ttu-id="1e81f-271">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1e81f-271">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="1e81f-272">Требования</span><span class="sxs-lookup"><span data-stu-id="1e81f-272">Requirements</span></span>



| <span data-ttu-id="1e81f-273">Требование</span><span class="sxs-lookup"><span data-stu-id="1e81f-273">Requirement</span></span> | <span data-ttu-id="1e81f-274">Значение</span><span class="sxs-lookup"><span data-stu-id="1e81f-274">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e81f-275">Клиент</span><span class="sxs-lookup"><span data-stu-id="1e81f-275">Client</span></span><br/> | <span data-ttu-id="1e81f-276">Windows XP, Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e81f-276">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="1e81f-277">Header</span><span class="sxs-lookup"><span data-stu-id="1e81f-277">Header</span></span><br/> | <dl> <span data-ttu-id="1e81f-278"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e81f-278"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="1e81f-279">DLL</span><span class="sxs-lookup"><span data-stu-id="1e81f-279">DLL</span></span><br/>    | <dl> <span data-ttu-id="1e81f-280"><dt>Wmvxencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e81f-280"><dt>Wmvxencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e81f-281">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e81f-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e81f-282">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="1e81f-282">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="1e81f-283">Реализация кодека</span><span class="sxs-lookup"><span data-stu-id="1e81f-283">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="1e81f-284">Идентификаторы GUID для подтипов видео</span><span class="sxs-lookup"><span data-stu-id="1e81f-284">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 
