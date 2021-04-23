---
description: Кодировщик Windows Media Video 9 кодирует видеопотоки.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Кодировщик Windows Media Video 9 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36ee5823c585d60ee74e75f99e8ec9b4d91f5cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721039"
---
# <a name="windows-media-video-9-encoder"></a><span data-ttu-id="1a52e-103">Кодировщик Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="1a52e-103">Windows Media Video 9 Encoder</span></span>

<span data-ttu-id="1a52e-104">Кодировщик Windows Media Video 9 кодирует видеопотоки.</span><span class="sxs-lookup"><span data-stu-id="1a52e-104">The Windows Media Video 9 encoder encodes video streams.</span></span> <span data-ttu-id="1a52e-105">Кодировщик поддерживает следующие четыре категории закодированных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1a52e-105">The encoder supports the following four categories of encoded output.</span></span>

-   <span data-ttu-id="1a52e-106">Простой профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="1a52e-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="1a52e-107">Основной профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="1a52e-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="1a52e-108">Расширенный профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="1a52e-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="1a52e-109">Изображение Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="1a52e-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="1a52e-110">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="1a52e-110">Class Identifier</span></span>

<span data-ttu-id="1a52e-111">Идентификатор класса (CLSID) для кодировщика видео Windows Media представлен константой **CLSID \_ CWMV9EncMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="1a52e-111">The class identifier (CLSID) for the Windows Media Video encoder is represented by the constant **CLSID\_CWMV9EncMediaObject**.</span></span> <span data-ttu-id="1a52e-112">Вы можете создать экземпляр кодировщика видео, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="1a52e-112">You can create an instance of the video encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="1a52e-113">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="1a52e-113">Interfaces</span></span>

<span data-ttu-id="1a52e-114">Объект видеокодировщика предоставляет интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="1a52e-114">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="1a52e-115">Видеокодировщик ведет себя как DMO или файл MFT в зависимости от того, какие интерфейсы вы получаете и какая версия Windows выполняется.</span><span class="sxs-lookup"><span data-stu-id="1a52e-115">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="1a52e-116">В следующей таблице показаны условия, при которых кодировщик видео ведет себя как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="1a52e-116">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="1a52e-117">Операционная система</span><span class="sxs-lookup"><span data-stu-id="1a52e-117">Operating system</span></span>            | <span data-ttu-id="1a52e-118">Поведение кодировщика</span><span class="sxs-lookup"><span data-stu-id="1a52e-118">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a52e-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1a52e-119">Windows XP</span></span>                  | <span data-ttu-id="1a52e-120">Кодировщик Windows Media Video всегда ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="1a52e-120">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="1a52e-121">Windows Vista и Windows 7</span><span class="sxs-lookup"><span data-stu-id="1a52e-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="1a52e-122">По умолчанию кодировщик видео Windows Media ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="1a52e-122">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="1a52e-123">Если вы получаете интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) для видеокодировщика, он ведет себя как файл MFT.</span><span class="sxs-lookup"><span data-stu-id="1a52e-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="1a52e-124">Форматы входных данных</span><span class="sxs-lookup"><span data-stu-id="1a52e-124">Input Formats</span></span>

<span data-ttu-id="1a52e-125">Кодировщик Windows Media Video поддерживает следующие входные подтипы носителей, когда он выступает в роли DMO.</span><span class="sxs-lookup"><span data-stu-id="1a52e-125">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="1a52e-126">МЕДИАСУБТИПЕ \_ ийув</span><span class="sxs-lookup"><span data-stu-id="1a52e-126">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="1a52e-127">МЕДИАСУБТИПЕ \_ I420</span><span class="sxs-lookup"><span data-stu-id="1a52e-127">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="1a52e-128">МЕДИАСУБТИПЕ \_ YV12</span><span class="sxs-lookup"><span data-stu-id="1a52e-128">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="1a52e-129">МЕДИАСУБТИПЕ \_ NV11</span><span class="sxs-lookup"><span data-stu-id="1a52e-129">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="1a52e-130">МЕДИАСУБТИПЕ \_ NV12</span><span class="sxs-lookup"><span data-stu-id="1a52e-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="1a52e-131">МЕДИАСУБТИПЕ \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="1a52e-131">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="1a52e-132">МЕДИАСУБТИПЕ \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="1a52e-132">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="1a52e-133">МЕДИАСУБТИПЕ \_ ивю</span><span class="sxs-lookup"><span data-stu-id="1a52e-133">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="1a52e-134">МЕДИАСУБТИПЕ \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="1a52e-134">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="1a52e-135">МЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="1a52e-135">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="1a52e-136">МЕДИАСУБТИПЕ \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="1a52e-136">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="1a52e-137">МЕДИАСУБТИПЕ \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="1a52e-137">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="1a52e-138">МЕДИАСУБТИПЕ \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="1a52e-138">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="1a52e-139">МЕДИАСУБТИПЕ \_</span><span class="sxs-lookup"><span data-stu-id="1a52e-139">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="1a52e-140">Кодировщик Windows Media Video поддерживает следующие входные подтипы носителя, когда он выступает в качестве MFT.</span><span class="sxs-lookup"><span data-stu-id="1a52e-140">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="1a52e-141">Мфвидеоформат \_ ийув</span><span class="sxs-lookup"><span data-stu-id="1a52e-141">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="1a52e-142">Мфвидеоформат \_ I420</span><span class="sxs-lookup"><span data-stu-id="1a52e-142">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="1a52e-143">Мфвидеоформат \_ YV12</span><span class="sxs-lookup"><span data-stu-id="1a52e-143">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="1a52e-144">Мфвидеоформат \_ NV11</span><span class="sxs-lookup"><span data-stu-id="1a52e-144">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="1a52e-145">Мфвидеоформат \_ NV12</span><span class="sxs-lookup"><span data-stu-id="1a52e-145">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="1a52e-146">Мфвидеоформат \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="1a52e-146">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="1a52e-147">Мфвидеоформат \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="1a52e-147">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="1a52e-148">Мфвидеоформат \_ ивю</span><span class="sxs-lookup"><span data-stu-id="1a52e-148">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="1a52e-149">Мфвидеоформат \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="1a52e-149">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="1a52e-150">Мфвидеоформат \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="1a52e-150">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="1a52e-151">Мфвидеоформат \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="1a52e-151">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="1a52e-152">Мфвидеоформат \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="1a52e-152">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="1a52e-153">Мфвидеоформат \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="1a52e-153">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="1a52e-154">МЕДИАСУБТИПЕ \_</span><span class="sxs-lookup"><span data-stu-id="1a52e-154">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="1a52e-155">Форматы выходных данных</span><span class="sxs-lookup"><span data-stu-id="1a52e-155">Output Formats</span></span>

<span data-ttu-id="1a52e-156">В следующей таблице показаны 4-символьные коды (Фаурккс), соответствующие категориям закодированных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1a52e-156">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded output.</span></span>



| <span data-ttu-id="1a52e-157">Категория</span><span class="sxs-lookup"><span data-stu-id="1a52e-157">Category</span></span>                               | <span data-ttu-id="1a52e-158">FOURCC</span><span class="sxs-lookup"><span data-stu-id="1a52e-158">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="1a52e-159">Простой профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="1a52e-159">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="1a52e-160">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="1a52e-160">"WMV3"</span></span>                                   |
| <span data-ttu-id="1a52e-161">Основной профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="1a52e-161">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="1a52e-162">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="1a52e-162">"WMV3"</span></span>                                   |
| <span data-ttu-id="1a52e-163">Расширенный профиль Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="1a52e-163">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="1a52e-164">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="1a52e-164">"WVC1"</span></span>                                   |
| <span data-ttu-id="1a52e-165">Изображение Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="1a52e-165">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="1a52e-166">"ВМВП" для 9,1, "WVP2" для 9,1 версии 2</span><span class="sxs-lookup"><span data-stu-id="1a52e-166">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

<span data-ttu-id="1a52e-167">Чтобы различать простой профиль и основной профиль, задайте свойство [**мфпкэй \_ декодеркомплекситирекуестед**](mfpkey-decodercomplexityrequestedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="1a52e-167">To distinguish between Simple Profile and Main Profile, set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property.</span></span>

## <a name="properties"></a><span data-ttu-id="1a52e-168">Свойства</span><span class="sxs-lookup"><span data-stu-id="1a52e-168">Properties</span></span>

<span data-ttu-id="1a52e-169">Кодировщик Windows Media Video 9 поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1a52e-169">The Windows Media Video 9 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1a52e-170">Свойство</span><span class="sxs-lookup"><span data-stu-id="1a52e-170">Property</span></span></th>
<th><span data-ttu-id="1a52e-171">Описание</span><span class="sxs-lookup"><span data-stu-id="1a52e-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a52e-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-173">Указывает дополнительную нагрузку в байтах на пакет, необходимую для контейнера, используемого для хранения сжатого содержимого.</span><span class="sxs-lookup"><span data-stu-id="1a52e-173">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="1a52e-174">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-174">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-175">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-175">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-176">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-178">Указывает среднюю частоту кадров содержимого видео в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="1a52e-178">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="1a52e-179">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-179">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-180">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-180">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-181">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-183">Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с средней скоростью (заданным <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="1a52e-183">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="1a52e-184">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-184">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-185">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-185">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-186">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1a52e-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-188">Указывает Дельта-увеличение между рисунком куантизер фрейма привязки и изображением куантизер в B-кадре.</span><span class="sxs-lookup"><span data-stu-id="1a52e-188">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span><br/> <dl> <span data-ttu-id="1a52e-189">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-189">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-190">Основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-190">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-191">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-191">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-193">Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с пиковой скоростью (заданное <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="1a52e-193">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="1a52e-194">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-194">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-195">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-195">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-196">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1a52e-196">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-198">Указывает, содержит ли закодированный поток видео значение полных буферов со всеми ключевыми кадрами.</span><span class="sxs-lookup"><span data-stu-id="1a52e-198">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="1a52e-199">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-199">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-200">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-200">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-201">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-201">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-203">Задает шаблон кодировки, используемый в начале группы изображений.</span><span class="sxs-lookup"><span data-stu-id="1a52e-203">Specifies the encoding pattern to use at the beginning of a group of pictures.</span></span><br/> <dl> <span data-ttu-id="1a52e-204">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="1a52e-205">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-205">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-206">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-206">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-208">Указывает число кадров видео, закодированных кодеком.</span><span class="sxs-lookup"><span data-stu-id="1a52e-208">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="1a52e-209">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-209">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-210">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-210">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-211">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-213">Указывает количество видеокадров, закодированных кодеком, который фактически содержит данные.</span><span class="sxs-lookup"><span data-stu-id="1a52e-213">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="1a52e-214">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-214">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-215">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-215">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-216">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-216">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-218">Это свойство заменяется <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1a52e-218">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-220">Указывает сложность алгоритма кодировщика.</span><span class="sxs-lookup"><span data-stu-id="1a52e-220">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="1a52e-221">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-221">Windows Vista and later.</span></span><br />
<span data-ttu-id="1a52e-222">Простой профиль, основной профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-222">Simple Profile, Main Profile.</span></span> <span data-ttu-id="1a52e-223">Расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-223">Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-224">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-224">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-226">Указывает тип оптимизации для микрокодека расширенного профиля Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="1a52e-226">Specifies the type of optimization to use for the Windows Media Video 9 Advanced Profile codec.</span></span><br/> <dl> <span data-ttu-id="1a52e-227">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-227">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-228">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-228">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-229">Запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-229">Write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-231">Задает числовое представление компромисса между плавностью движения и качеством изображения в выходных данных кодека.</span><span class="sxs-lookup"><span data-stu-id="1a52e-231">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="1a52e-232">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-232">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-233">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-233">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-234">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-234">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-236">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1a52e-236">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-238">Указывает шаблон соответствия устройства, которому соответствует закодированное содержимое.</span><span class="sxs-lookup"><span data-stu-id="1a52e-238">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="1a52e-239">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-239">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-240">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-240">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-241">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-241">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-243">Указывает шаблон соответствия устройств, который вы хотите использовать для кодирования видео.</span><span class="sxs-lookup"><span data-stu-id="1a52e-243">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="1a52e-244">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-244">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-245">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-245">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-246">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-246">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-248">Указывает метод, используемый для кодирования сведений о векторе движения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-248">Specifies the method used to encode the motion vector information.</span></span><br/> <dl> <span data-ttu-id="1a52e-249">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-249">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-250">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-250">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-251">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-251">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-253">Указывает, будет ли кодек использовать фильтр шума при кодировании.</span><span class="sxs-lookup"><span data-stu-id="1a52e-253">Specifies whether the codec will use the noise filter when encoding.</span></span><br/> <dl> <span data-ttu-id="1a52e-254">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-254">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-255">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-255">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-256">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-256">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-258">Задает требуемый уровень качества для кодирования с переменной скоростью (1 проход) с учетом качества (с частотой VBR).</span><span class="sxs-lookup"><span data-stu-id="1a52e-258">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="1a52e-259">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="1a52e-260">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-260">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-261">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-261">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-263">Указывает число кадров видео, отброшенных во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="1a52e-263">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="1a52e-264">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-264">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-265">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-265">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-266">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-266">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-268">Задает конец прохода кодирования.</span><span class="sxs-lookup"><span data-stu-id="1a52e-268">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="1a52e-269">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-269">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-270">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-270">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-271">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-271">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-273">Задает промежуточную высоту кадра для кодированного видео.</span><span class="sxs-lookup"><span data-stu-id="1a52e-273">Specifies an intermediate frame height for encoded video.</span></span><br/> <dl> <span data-ttu-id="1a52e-274">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-274">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-275">Расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-275">Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-276">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-278">Задает промежуточную ширину кадра для кодированного видео.</span><span class="sxs-lookup"><span data-stu-id="1a52e-278">Specifies an intermediate frame width for encoded video.</span></span><br/> <dl> <span data-ttu-id="1a52e-279">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-279">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-280">Расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-280">Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-281">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-283">Указывает, должен ли кодек использовать медианную фильтрацию во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="1a52e-283">Specifies whether the codec should use median filtering during encoding.</span></span><br/> <dl> <span data-ttu-id="1a52e-284">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-284">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-285">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-285">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-286">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-286">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-288">Указывает FOURCC, определяющую кодировщик, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="1a52e-288">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="1a52e-289">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-289">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-290">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-290">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-291">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-291">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-293">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="1a52e-293">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-295">Указывает, разрешено ли кодировщику удалять фреймы.</span><span class="sxs-lookup"><span data-stu-id="1a52e-295">Specifies whether the encoder is allowed to drop frames.</span></span><br/> <dl> <span data-ttu-id="1a52e-296">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-296">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-297">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-297">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-298">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-298">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-300">Указывает, следует ли использовать чередование выходных данных кодека.</span><span class="sxs-lookup"><span data-stu-id="1a52e-300">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="1a52e-301">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-301">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-302">Расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-302">Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-303">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-303">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-305">Указывает максимальное время в миллисекундах между опорными кадрами в выходных коде.</span><span class="sxs-lookup"><span data-stu-id="1a52e-305">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="1a52e-306">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-306">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-307">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-307">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-308">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-308">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-310">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1a52e-310">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-312">Указывает число кадров после текущего кадра, которое будет вычислено кодеком перед кодированием текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="1a52e-312">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span><br/> <dl> <span data-ttu-id="1a52e-313">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-313">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-314">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-314">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-315">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-315">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-317">Указывает, должен ли кодек использовать фильтр для деблокировки в процессе кодирования.</span><span class="sxs-lookup"><span data-stu-id="1a52e-317">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span><br/> <dl> <span data-ttu-id="1a52e-318">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-318">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-319">Основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-319">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-320">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-320">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-322">Указывает метод стоимости, используемый кодеком для определения используемого режима макроблокк.</span><span class="sxs-lookup"><span data-stu-id="1a52e-322">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span><br/> <dl> <span data-ttu-id="1a52e-323">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-323">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-324">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-324">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-325">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-325">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-327">Указывает метод, используемый для сопоставления движения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-327">Specifies the method to use for motion matching.</span></span><br/> <dl> <span data-ttu-id="1a52e-328">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-328">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-329">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-329">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-330">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-330">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-332">Указывает типы видеоданных, используемых в операциях поиска движения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-332">Specifies the types of video information that are used in motion search operations.</span></span><br/> <dl> <span data-ttu-id="1a52e-333">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-333">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-334">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-334">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-335">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-335">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-337">Указывает диапазон, используемый при поиске движения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-337">Specifies the range used in motion searches.</span></span><br/> <dl> <span data-ttu-id="1a52e-338">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-338">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-339">Основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-339">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-340">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-340">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-342">Указывает, должен ли кодек попытаться обнаружить шумы в кадрах и удалить их.</span><span class="sxs-lookup"><span data-stu-id="1a52e-342">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span><br/> <dl> <span data-ttu-id="1a52e-343">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-343">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-344">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-344">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-345">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-345">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-347">Задает число двунаправленных прогнозирующих кадров (B-кадров).</span><span class="sxs-lookup"><span data-stu-id="1a52e-347">Specifies the number of bidirectional predictive frames (B-frames).</span></span><br/> <dl> <span data-ttu-id="1a52e-348">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-348">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-349">Основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-349">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-350">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-350">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-352">Указывает количество потоков, которые кодек будет использовать для кодирования.</span><span class="sxs-lookup"><span data-stu-id="1a52e-352">Specifies the number of threads that the codec will use for encoding.</span></span><br/> <dl> <span data-ttu-id="1a52e-353">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-353">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-354">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-354">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-355">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-355">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-357">Указывает максимальное число проходов, поддерживаемое кодеком.</span><span class="sxs-lookup"><span data-stu-id="1a52e-357">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="1a52e-358">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-358">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-359">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-359">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-360">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-360">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-362">Указывает число проходов, которые кодек будет использовать для кодирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="1a52e-362">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="1a52e-363">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-363">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-364">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-364">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-365">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1a52e-365">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-367">Указывает, должен ли кодек использовать консервативную оптимизацию искусственного при кодировании.</span><span class="sxs-lookup"><span data-stu-id="1a52e-367">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span><br/> <dl> <span data-ttu-id="1a52e-368">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-368">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-369">Основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-369">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-370">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-370">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-372">Указывает, создает ли кодировщик фиктивные записи кадра в битовом потоке для повторяющихся кадров.</span><span class="sxs-lookup"><span data-stu-id="1a52e-372">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="1a52e-373">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-373">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-374">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-374">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-375">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-375">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-377">Указывает QP.</span><span class="sxs-lookup"><span data-stu-id="1a52e-377">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="1a52e-378">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-378">Windows Vista and later.</span></span><br />
<span data-ttu-id="1a52e-379">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-379">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-380">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-380">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-382">Указывает степень, до которой кодек должен уменьшить действующий цветовой диапазон видео.</span><span class="sxs-lookup"><span data-stu-id="1a52e-382">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span><br/> <dl> <span data-ttu-id="1a52e-383">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-383">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-384">Расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-384">Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-385">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-385">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-387">Указывает среднюю скорость потока в битах в секунду, используемую для 2-проходной кодировки с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="1a52e-387">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="1a52e-388">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-388">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-389">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-389">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-390">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1a52e-390">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-392">Указывает, использует ли кодировщик Поиск по подпикселям МВ на основе удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1a52e-392">Specifies whether the encoder uses RD-based sub-pixel MV search.</span></span> <br/> <dl> <span data-ttu-id="1a52e-393">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-393">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-394">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-394">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-395">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-395">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-397">Для повторной кодировки сегмента указывает размер буфера.</span><span class="sxs-lookup"><span data-stu-id="1a52e-397">For segment re-encoding, specifies the buffer size.</span></span><br/> <dl> <span data-ttu-id="1a52e-398">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-398">Windows Vista and later.</span></span><br />
<span data-ttu-id="1a52e-399">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-399">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-400">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-400">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-402">Для повторной кодировки сегмента указывает длительность сегмента для повторной кодировки.</span><span class="sxs-lookup"><span data-stu-id="1a52e-402">For segment re-encoding, specifies the duration of the segment to be re-encoded.</span></span><br/> <dl> <span data-ttu-id="1a52e-403">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-403">Windows Vista and later.</span></span><br />
<span data-ttu-id="1a52e-404">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-404">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-405">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-405">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-407">Для повторной кодировки сегмента указывает куантизер кадра перед начальным сегментом.</span><span class="sxs-lookup"><span data-stu-id="1a52e-407">For segment re-encoding, specifies the quantizer of the frame prior to the starting segment.</span></span><br/> <dl> <span data-ttu-id="1a52e-408">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-408">Windows Vista and later.</span></span><br />
<span data-ttu-id="1a52e-409">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-409">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-410">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-410">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-412">Для повторной кодировки сегмента задает заполнение начального буфера.</span><span class="sxs-lookup"><span data-stu-id="1a52e-412">For segment re-encoding, specifies the starting buffer fullness.</span></span><br/> <dl> <span data-ttu-id="1a52e-413">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-413">Windows Vista and later.</span></span><br />
<span data-ttu-id="1a52e-414">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-414">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-415">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-415">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-417">Указывает пиковую скорость потока (в битах в секунду), используемую для ограниченного 2-прохода переменной-разрядной скорости (VBR).</span><span class="sxs-lookup"><span data-stu-id="1a52e-417">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="1a52e-418">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-418">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-419">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-419">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-420">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1a52e-420">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-422">Указывает число кадров видео, переданных кодировщику во время процесса кодирования.</span><span class="sxs-lookup"><span data-stu-id="1a52e-422">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="1a52e-423">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-423">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-424">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-424">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-425">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1a52e-425">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-427">Указывает, будет ли кодек использовать кодирование с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="1a52e-427">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="1a52e-428">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-428">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-429">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-429">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-430">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1a52e-430">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-432">Задает реальный уровень качества для кодирования с переменной скоростью (1 проход) с учетом качества (с частотой VBR).</span><span class="sxs-lookup"><span data-stu-id="1a52e-432">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="1a52e-433">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-433">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-434">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-434">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-435">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-435">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-437">Указывает, будет ли кодек использовать оптимизацию масштабирования видео.</span><span class="sxs-lookup"><span data-stu-id="1a52e-437">Specifies whether the codec will use video scaling optimization.</span></span><br/> <dl> <span data-ttu-id="1a52e-438">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-438">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-439">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-439">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-440">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-440">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-442">Указывает объем содержимого в миллисекундах, который может поместиться в буфер модели.</span><span class="sxs-lookup"><span data-stu-id="1a52e-442">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="1a52e-443">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-443">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-444">Расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-444">Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-445">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-445">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-447">Для повторной кодировки сегмента указывает закрытые данные кодека файла, для которого выполняется повторная кодировка.</span><span class="sxs-lookup"><span data-stu-id="1a52e-447">For segment re-encoding, specifies the codec private data of the file that is being re-encoded.</span></span><br/> <dl> <span data-ttu-id="1a52e-448">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-448">Windows Vista and later.</span></span><br />
<span data-ttu-id="1a52e-449">Простой профиль, основной профиль, расширенный профиль, изображение.</span><span class="sxs-lookup"><span data-stu-id="1a52e-449">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="1a52e-450">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-450">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a52e-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-452">Указывает тип логики, которую кодек будет использовать для обнаружения чередующихся исходных видео.</span><span class="sxs-lookup"><span data-stu-id="1a52e-452">Specifies the type of logic that the codec will use to detect interlaced source video.</span></span><br/> <dl> <span data-ttu-id="1a52e-453">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-453">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-454">Расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-454">Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-455">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="1a52e-455">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a52e-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a52e-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="1a52e-457">Указывает число пропущенных видеокадров, так как они являлись дубликатами предыдущих кадров.</span><span class="sxs-lookup"><span data-stu-id="1a52e-457">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="1a52e-458">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="1a52e-458">Windows XP and later.</span></span><br />
<span data-ttu-id="1a52e-459">Простой профиль, основной профиль, расширенный профиль.</span><span class="sxs-lookup"><span data-stu-id="1a52e-459">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="1a52e-460">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1a52e-460">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="1a52e-461">Требования</span><span class="sxs-lookup"><span data-stu-id="1a52e-461">Requirements</span></span>



| <span data-ttu-id="1a52e-462">Требование</span><span class="sxs-lookup"><span data-stu-id="1a52e-462">Requirement</span></span> | <span data-ttu-id="1a52e-463">Значение</span><span class="sxs-lookup"><span data-stu-id="1a52e-463">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a52e-464">Клиент</span><span class="sxs-lookup"><span data-stu-id="1a52e-464">Client</span></span><br/> | <span data-ttu-id="1a52e-465">Windows XP, Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="1a52e-465">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="1a52e-466">Header</span><span class="sxs-lookup"><span data-stu-id="1a52e-466">Header</span></span><br/> | <dl> <span data-ttu-id="1a52e-467"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a52e-467"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="1a52e-468">DLL</span><span class="sxs-lookup"><span data-stu-id="1a52e-468">DLL</span></span><br/>    | <dl> <span data-ttu-id="1a52e-469"><dt>Wmvencod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a52e-469"><dt>Wmvencod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a52e-470">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a52e-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a52e-471">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="1a52e-471">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="1a52e-472">Реализация кодека</span><span class="sxs-lookup"><span data-stu-id="1a52e-472">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
