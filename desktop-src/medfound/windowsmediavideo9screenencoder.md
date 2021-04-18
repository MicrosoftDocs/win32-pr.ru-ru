---
description: Экранный кодировщик Windows Media Video 9 оптимизирован для кодирования последовательных снимков экрана от компьютерных мониторов.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Кодировщик экрана Windows Media видео 9 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708456"
---
# <a name="windows-media-video-9-screen-encoder"></a><span data-ttu-id="d746c-103">Кодировщик экрана Windows Media видео 9</span><span class="sxs-lookup"><span data-stu-id="d746c-103">Windows Media Video 9 Screen Encoder</span></span>

<span data-ttu-id="d746c-104">Экранный кодировщик Windows Media Video 9 оптимизирован для кодирования последовательных снимков экрана от компьютерных мониторов.</span><span class="sxs-lookup"><span data-stu-id="d746c-104">The Windows Media Video 9 Screen encoder is optimized for encoding sequential screen shots from computer monitors.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="d746c-105">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="d746c-105">Class Identifier</span></span>

<span data-ttu-id="d746c-106">Идентификатор класса (CLSID) для кодировщика экрана Windows Media Video 9 представлен константой **CLSID \_ CMSSCEncMediaObject2**.</span><span class="sxs-lookup"><span data-stu-id="d746c-106">The class identifier (CLSID) for the Windows Media Video 9 Screen encoder is represented by the constant **CLSID\_CMSSCEncMediaObject2**.</span></span> <span data-ttu-id="d746c-107">Экземпляр кодировщика можно создать, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="d746c-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="d746c-108">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="d746c-108">Input Types</span></span>

<span data-ttu-id="d746c-109">Кодировщик экрана версии 9 поддерживает следующие типы входных данных, когда он используется в качестве объекта мультимедиа DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="d746c-109">The following input types are supported by the Version 9 Screen encoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="d746c-110">МЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="d746c-110">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="d746c-111">МЕДИАСУБТИПЕ \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d746c-111">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="d746c-112">МЕДИАСУБТИПЕ \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="d746c-112">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="d746c-113">МЕДИАСУБТИПЕ \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d746c-113">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="d746c-114">МЕДИАСУБТИПЕ \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d746c-114">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="d746c-115">МЕДИАСУБТИПЕ \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d746c-115">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="d746c-116">Кодировщик экрана версии 9 поддерживает следующие типы входных данных, когда он используется в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="d746c-116">The following input types are supported by the Version 9 Screen encoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="d746c-117">Мфвидеоформат \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="d746c-117">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="d746c-118">Мфвидеоформат \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d746c-118">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="d746c-119">Мфвидеоформат \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="d746c-119">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="d746c-120">Мфвидеоформат \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d746c-120">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="d746c-121">Мфвидеоформат \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d746c-121">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="d746c-122">Мфвидеоформат \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d746c-122">MFVideoFormat\_RGB8</span></span>

## <a name="output-types"></a><span data-ttu-id="d746c-123">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="d746c-123">Output Types</span></span>

<span data-ttu-id="d746c-124">Код из четырех символов (FOURCC) для содержимого с видео Windows Media версии 9 — "MSS2".</span><span class="sxs-lookup"><span data-stu-id="d746c-124">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="d746c-125">Кодировщик экрана версии 9 поддерживает следующие типы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d746c-125">The following output types are supported by the Version 9 Screen encoder.</span></span>

-   <span data-ttu-id="d746c-126">МЕДИАСУБТИПЕ \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="d746c-126">MEDIASUBTYPE\_MSS2</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="d746c-127">Свойства кодировщика</span><span class="sxs-lookup"><span data-stu-id="d746c-127">Encoder Properties</span></span>

<span data-ttu-id="d746c-128">Кодировщик Windows Media Video 9 экрана поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d746c-128">The Windows Media Video 9 Screen encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d746c-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="d746c-129">Property</span></span></th>
<th><span data-ttu-id="d746c-130">Описание</span><span class="sxs-lookup"><span data-stu-id="d746c-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d746c-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="d746c-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span></span></td>
<td><span data-ttu-id="d746c-132">Указывает накладные расходы (в байтах на пакет), необходимые для контейнера, используемого для хранения сжатого содержимого.</span><span class="sxs-lookup"><span data-stu-id="d746c-132">Specifies the overhead, in bytes per packet, required for the container that is used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="d746c-133">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-133">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-134">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="d746c-134">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span><span class="sxs-lookup"><span data-stu-id="d746c-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span></span></td>
<td><span data-ttu-id="d746c-136">Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с средней скоростью (заданным <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span><span class="sxs-lookup"><span data-stu-id="d746c-136">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span></span><br/> <dl> <span data-ttu-id="d746c-137">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-137">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-138">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d746c-138">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d746c-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span><span class="sxs-lookup"><span data-stu-id="d746c-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span></span></td>
<td><span data-ttu-id="d746c-140">Указывает окно буфера (в миллисекундах) для потока с переменным числом переменных с переменной скоростью (VBR) с пиковой скоростью (заданное <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span><span class="sxs-lookup"><span data-stu-id="d746c-140">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span></span><br/> <dl> <span data-ttu-id="d746c-141">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-141">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-142">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d746c-142">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span><span class="sxs-lookup"><span data-stu-id="d746c-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span></span></td>
<td><span data-ttu-id="d746c-144">Указывает, содержит ли закодированный поток видео значение полных буферов со всеми ключевыми кадрами.</span><span class="sxs-lookup"><span data-stu-id="d746c-144">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="d746c-145">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-145">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-146">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d746c-146">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d746c-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="d746c-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span></span></td>
<td><span data-ttu-id="d746c-148">Указывает число кадров видео, закодированных кодеком.</span><span class="sxs-lookup"><span data-stu-id="d746c-148">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="d746c-149">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-149">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-150">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d746c-150">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="d746c-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span></span></td>
<td><span data-ttu-id="d746c-152">Указывает количество видеокадров, закодированных кодеком, который фактически содержит данные.</span><span class="sxs-lookup"><span data-stu-id="d746c-152">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="d746c-153">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-153">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-154">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d746c-154">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d746c-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span><span class="sxs-lookup"><span data-stu-id="d746c-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span></span></td>
<td><span data-ttu-id="d746c-156">Это свойство заменяется <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span><span class="sxs-lookup"><span data-stu-id="d746c-156">This property is superseded by <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span><span class="sxs-lookup"><span data-stu-id="d746c-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span></span></td>
<td><span data-ttu-id="d746c-158">Указывает сложность алгоритма кодировщика.</span><span class="sxs-lookup"><span data-stu-id="d746c-158">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="d746c-159">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="d746c-160">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="d746c-160">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d746c-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span><span class="sxs-lookup"><span data-stu-id="d746c-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span></span></td>
<td><span data-ttu-id="d746c-162">Задает числовое представление компромисса между плавностью движения и качеством изображения в выходных данных кодека.</span><span class="sxs-lookup"><span data-stu-id="d746c-162">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="d746c-163">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-163">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-164">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="d746c-164">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="d746c-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span></span></td>
<td><span data-ttu-id="d746c-166">Указывает число кадров видео, отброшенных во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="d746c-166">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="d746c-167">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-167">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-168">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d746c-168">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d746c-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span><span class="sxs-lookup"><span data-stu-id="d746c-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span></span></td>
<td><span data-ttu-id="d746c-170">Задает конец прохода кодирования.</span><span class="sxs-lookup"><span data-stu-id="d746c-170">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="d746c-171">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-171">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-172">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="d746c-172">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span><span class="sxs-lookup"><span data-stu-id="d746c-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span></span></td>
<td><span data-ttu-id="d746c-174">Указывает FOURCC, определяющую кодировщик, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="d746c-174">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="d746c-175">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-175">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-176">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="d746c-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d746c-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span><span class="sxs-lookup"><span data-stu-id="d746c-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span></span></td>
<td><span data-ttu-id="d746c-178">Указывает максимальное время в миллисекундах между опорными кадрами в выходных коде.</span><span class="sxs-lookup"><span data-stu-id="d746c-178">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="d746c-179">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-179">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-180">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="d746c-180">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span><span class="sxs-lookup"><span data-stu-id="d746c-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span></span></td>
<td><span data-ttu-id="d746c-182">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="d746c-182">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d746c-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span><span class="sxs-lookup"><span data-stu-id="d746c-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span></span></td>
<td><span data-ttu-id="d746c-184">Указывает максимальное число проходов, поддерживаемое кодеком.</span><span class="sxs-lookup"><span data-stu-id="d746c-184">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="d746c-185">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-185">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-186">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d746c-186">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span><span class="sxs-lookup"><span data-stu-id="d746c-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span></span></td>
<td><span data-ttu-id="d746c-188">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-188">Windows XP and later.</span></span> <span data-ttu-id="d746c-189">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d746c-189">Read/write.</span></span><br/> <span data-ttu-id="d746c-190">Указывает число проходов, которые кодек будет использовать для кодирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="d746c-190">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="d746c-191">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-191">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-192">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d746c-192">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d746c-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="d746c-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span></span></td>
<td><span data-ttu-id="d746c-194">Указывает QP.</span><span class="sxs-lookup"><span data-stu-id="d746c-194">Specifies QP.</span></span> <span data-ttu-id="d746c-195">Возможные значения — от 1,0 до 31,0.</span><span class="sxs-lookup"><span data-stu-id="d746c-195">Possible values are 1.0 through 31.0.</span></span><br/> <dl> <span data-ttu-id="d746c-196">Windows Vista и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-196">Windows Vista and later.</span></span><br />
<span data-ttu-id="d746c-197">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="d746c-197">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span><span class="sxs-lookup"><span data-stu-id="d746c-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span></span></td>
<td><span data-ttu-id="d746c-199">Указывает среднюю скорость потока в битах в секунду, используемую для 2-проходной кодировки с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="d746c-199">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d746c-200">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-200">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-201">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d746c-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d746c-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span><span class="sxs-lookup"><span data-stu-id="d746c-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span></span></td>
<td><span data-ttu-id="d746c-203">Указывает пиковую скорость потока (в битах в секунду), используемую для ограниченного 2-прохода с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="d746c-203">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d746c-204">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-204">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-205">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d746c-205">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="d746c-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span></span></td>
<td><span data-ttu-id="d746c-207">Указывает число кадров видео, переданных кодировщику во время процесса кодирования.</span><span class="sxs-lookup"><span data-stu-id="d746c-207">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="d746c-208">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-208">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-209">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d746c-209">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d746c-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span><span class="sxs-lookup"><span data-stu-id="d746c-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span></span></td>
<td><span data-ttu-id="d746c-211">Указывает, будет ли кодек использовать кодирование с переменной скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="d746c-211">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d746c-212">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-212">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-213">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d746c-213">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span><span class="sxs-lookup"><span data-stu-id="d746c-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span></span></td>
<td><span data-ttu-id="d746c-215">Задает реальный уровень качества для кодирования с переменной скоростью (1 проход) с учетом качества (с частотой VBR).</span><span class="sxs-lookup"><span data-stu-id="d746c-215">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="d746c-216">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-216">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-217">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="d746c-217">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d746c-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="d746c-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span></span></td>
<td><span data-ttu-id="d746c-219">Объем содержимого в миллисекундах, который может поместиться в буфер модели.</span><span class="sxs-lookup"><span data-stu-id="d746c-219">The amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="d746c-220">Windows XP и более поздние версии,</span><span class="sxs-lookup"><span data-stu-id="d746c-220">Windows XP and later,</span></span><br />
<span data-ttu-id="d746c-221">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="d746c-221">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d746c-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="d746c-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span></span></td>
<td><span data-ttu-id="d746c-223">Указывает число пропущенных видеокадров, так как они являлись дубликатами предыдущих кадров.</span><span class="sxs-lookup"><span data-stu-id="d746c-223">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="d746c-224">Windows XP и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="d746c-224">Windows XP and later.</span></span><br />
<span data-ttu-id="d746c-225">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d746c-225">Read-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="d746c-226">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d746c-226">Remarks</span></span>

<span data-ttu-id="d746c-227">Объект кодировщика экрана предоставляет интерфейс **имедиаобжект** , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс **имфтрансформ** , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="d746c-227">A screen encoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="d746c-228">Кодировщик экрана ведет себя как DMO или MFT в зависимости от того, какие интерфейсы вы получаете и какая версия Windows выполняется.</span><span class="sxs-lookup"><span data-stu-id="d746c-228">A screen encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="d746c-229">В следующей таблице показаны условия, при которых кодировщик экрана ведет себя как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="d746c-229">The following table shows the conditions under which a screen encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="d746c-230">Операционная система</span><span class="sxs-lookup"><span data-stu-id="d746c-230">Operating system</span></span>            | <span data-ttu-id="d746c-231">Поведение кодировщика</span><span class="sxs-lookup"><span data-stu-id="d746c-231">Encoder behavior</span></span>                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d746c-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d746c-232">Windows XP</span></span>                  | <span data-ttu-id="d746c-233">Кодировщик экрана Windows Media всегда ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="d746c-233">A Windows Media Screen encoder always behaves as a DMO.</span></span>                                                                                             |
| <span data-ttu-id="d746c-234">Windows Vista и Windows 7</span><span class="sxs-lookup"><span data-stu-id="d746c-234">Windows Vista and Windows 7</span></span> | <span data-ttu-id="d746c-235">По умолчанию кодировщик экрана Windows Media ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="d746c-235">By default, a Windows Media Screen encoder behaves as a DMO.</span></span> <span data-ttu-id="d746c-236">При получении интерфейса **имфтрансформ** на экране кодировщика он ведет себя как MFT.</span><span class="sxs-lookup"><span data-stu-id="d746c-236">If you obtain an **IMFTransform** interface on a screen encoder, it behaves as an MFT.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d746c-237">Требования</span><span class="sxs-lookup"><span data-stu-id="d746c-237">Requirements</span></span>



| <span data-ttu-id="d746c-238">Требование</span><span class="sxs-lookup"><span data-stu-id="d746c-238">Requirement</span></span> | <span data-ttu-id="d746c-239">Значение</span><span class="sxs-lookup"><span data-stu-id="d746c-239">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d746c-240">Клиент</span><span class="sxs-lookup"><span data-stu-id="d746c-240">Client</span></span><br/> | <span data-ttu-id="d746c-241">Windows XP, Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="d746c-241">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="d746c-242">Header</span><span class="sxs-lookup"><span data-stu-id="d746c-242">Header</span></span><br/> | <dl> <span data-ttu-id="d746c-243"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d746c-243"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="d746c-244">DLL</span><span class="sxs-lookup"><span data-stu-id="d746c-244">DLL</span></span><br/>    | <dl> <span data-ttu-id="d746c-245"><dt>Wmvsencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d746c-245"><dt>Wmvsencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d746c-246">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d746c-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d746c-247">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="d746c-247">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="d746c-248">Реализация кодека</span><span class="sxs-lookup"><span data-stu-id="d746c-248">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="d746c-249">Использование экранного видеокодека Windows Media видео 9</span><span class="sxs-lookup"><span data-stu-id="d746c-249">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="d746c-250">Декодер экрана Windows Media видео 9</span><span class="sxs-lookup"><span data-stu-id="d746c-250">Windows Media Video 9 Screen Decoder</span></span>](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




