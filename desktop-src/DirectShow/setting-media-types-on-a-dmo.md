---
description: Настройка типов мультимедиа для DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Настройка типов мультимедиа для DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684781"
---
# <a name="setting-media-types-on-a-dmo"></a><span data-ttu-id="fe69f-103">Настройка типов мультимедиа для DMO</span><span class="sxs-lookup"><span data-stu-id="fe69f-103">Setting Media Types on a DMO</span></span>

<span data-ttu-id="fe69f-104">Прежде чем DMO сможет обработать какие-либо данные, клиент должен задать тип носителя для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="fe69f-104">Before a DMO can process any data, the client must set the media type for each stream.</span></span> <span data-ttu-id="fe69f-105">(Для этого правила существует одно небольшое исключение; см. [дополнительные потоки](optional-streams.md).) Чтобы узнать число потоков, вызовите метод [**имедиаобжект:: жетстреамкаунт**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) :</span><span class="sxs-lookup"><span data-stu-id="fe69f-105">(There is one minor exception to this rule; see [Optional Streams](optional-streams.md).) To find the number of streams, call the [**IMediaObject::GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) method:</span></span>


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



<span data-ttu-id="fe69f-106">Этот метод возвращает два значения, число входов и число выходов.</span><span class="sxs-lookup"><span data-stu-id="fe69f-106">This method returns two values, the number of inputs and the number of outputs.</span></span> <span data-ttu-id="fe69f-107">Эти значения фиксируются в течение времени существования DMO.</span><span class="sxs-lookup"><span data-stu-id="fe69f-107">These values are fixed for the lifetime of the DMO.</span></span>

<span data-ttu-id="fe69f-108">**Предпочтительные типы**</span><span class="sxs-lookup"><span data-stu-id="fe69f-108">**Preferred Types**</span></span>

<span data-ttu-id="fe69f-109">Для каждого потока DMO назначает список возможных типов носителей в порядке предпочтения.</span><span class="sxs-lookup"><span data-stu-id="fe69f-109">For every stream, the DMO assigns a list of possible media types, in order of preference.</span></span> <span data-ttu-id="fe69f-110">Например, в этом порядке предпочтительными типами могут быть 32-RGB, 24-разрядный RGB и 16-разрядный RGB.</span><span class="sxs-lookup"><span data-stu-id="fe69f-110">For example, the preferred types might be 32-RGB, 24-bit RGB, and 16-bit RGB, in that order.</span></span> <span data-ttu-id="fe69f-111">Когда клиент задает типы носителей, он может использовать эти списки в качестве подсказки.</span><span class="sxs-lookup"><span data-stu-id="fe69f-111">When the client sets the media types, it can use these lists as a hint.</span></span> <span data-ttu-id="fe69f-112">Чтобы получить предпочтительный тип для потока, вызовите метод [**имедиаобжект:: жетинпуттипе**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) или [**Имедиаобжект:: жетаутпуттипе**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) .</span><span class="sxs-lookup"><span data-stu-id="fe69f-112">To retrieve a preferred type for a stream, call the [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) method or [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) method.</span></span> <span data-ttu-id="fe69f-113">Укажите номер потока и значение индекса для типа (начиная с нуля).</span><span class="sxs-lookup"><span data-stu-id="fe69f-113">Specify the stream number and an index value for the type (starting from zero).</span></span> <span data-ttu-id="fe69f-114">Например, следующий код извлекает первый предпочтительный тип из первого входного потока:</span><span class="sxs-lookup"><span data-stu-id="fe69f-114">For example, the following code retrieves the first preferred type from the first input stream:</span></span>


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="fe69f-115">Чтобы перечислить все предпочтительные типы мультимедиа в заданном потоке, используйте цикл, увеличивающий индекс типа до тех пор, пока метод \_ не вернет DMO \_ \_ \_ , а не больше элементов, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="fe69f-115">To enumerate all of the preferred media types on a given stream, use a loop that increments the type index until the method returns DMO\_E\_NO\_MORE\_ITEMS, as shown in the following example:</span></span>


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



<span data-ttu-id="fe69f-116">Обратите внимание на следующие моменты о предпочтительных типах:</span><span class="sxs-lookup"><span data-stu-id="fe69f-116">You should note the following points about preferred types:</span></span>

-   <span data-ttu-id="fe69f-117">DMO может возвращать тип, не имеющий блока Format.</span><span class="sxs-lookup"><span data-stu-id="fe69f-117">The DMO might return a type that has no format block.</span></span> <span data-ttu-id="fe69f-118">Например, DMO может указать тип видео, например 24-разрядный RGB, без указания ширины и высоты изображения.</span><span class="sxs-lookup"><span data-stu-id="fe69f-118">For example, a DMO could specify a video type, such as 24-bit RGB, without providing the width and height of the image.</span></span> <span data-ttu-id="fe69f-119">Однако при задании типа необходимо указать полный блок формата.</span><span class="sxs-lookup"><span data-stu-id="fe69f-119">When you set the type, however, you must provide a complete format block.</span></span> <span data-ttu-id="fe69f-120">(Некоторые типы носителей, например MIDI, никогда не нуждаются в блоке формата, в этом случае это замечание не применяется.)</span><span class="sxs-lookup"><span data-stu-id="fe69f-120">(Some media types, such as MIDI, never require a format block, in which case this remark does not apply.)</span></span>
-   <span data-ttu-id="fe69f-121">DMO не требуется поддерживать каждое сочетание предпочтительных типов, которые он возвращает.</span><span class="sxs-lookup"><span data-stu-id="fe69f-121">The DMO is not required to support every combination of preferred types that it returns.</span></span> <span data-ttu-id="fe69f-122">Например, если у DMO есть два потока, и каждый поток имеет четыре основных типа, существует 16 возможных сочетаний, но не все они гарантированно являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="fe69f-122">For example, if a DMO has two streams, and each stream has four preferred types, there are 16 possible combinations, but not all of them are guaranteed to be valid.</span></span>
-   <span data-ttu-id="fe69f-123">Когда клиент задает тип носителя для одного потока, DMO может обновить предпочтительные типы для других потоков, чтобы отразить новое состояние.</span><span class="sxs-lookup"><span data-stu-id="fe69f-123">When the client sets the media type for one stream, the DMO might update the preferred types for other streams to reflect the new state.</span></span> <span data-ttu-id="fe69f-124">Однако это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="fe69f-124">It is not required to do so, however.</span></span>
-   <span data-ttu-id="fe69f-125">Для некоторых потоков DMO может не предлагать никаких предпочтительных типов.</span><span class="sxs-lookup"><span data-stu-id="fe69f-125">For some streams, the DMO might not offer any preferred types.</span></span> <span data-ttu-id="fe69f-126">Как правило, DMO должен предлагать по крайней мере некоторые предпочтительные типы в некоторых потоках.</span><span class="sxs-lookup"><span data-stu-id="fe69f-126">Typically, a DMO should offer at least some preferred types on some streams.</span></span>
-   <span data-ttu-id="fe69f-127">DMO не требуется для предоставления полного списка типов мультимедиа, которые он может принять.</span><span class="sxs-lookup"><span data-stu-id="fe69f-127">The DMO is not required to offer a complete list of the media types it can accept.</span></span> <span data-ttu-id="fe69f-128">Могут существовать "необъявленные" типы, которые поддерживаются DMO, но не предлагаются в качестве предпочитаемых типов.</span><span class="sxs-lookup"><span data-stu-id="fe69f-128">There might be "unadvertised" types that the DMO supports but does not offer as preferred types.</span></span>

<span data-ttu-id="fe69f-129">Вкратце, клиент должен рассматривать предпочтительные типы как только рекомендации.</span><span class="sxs-lookup"><span data-stu-id="fe69f-129">In short, the client should treat the preferred types as guidelines only.</span></span> <span data-ttu-id="fe69f-130">Единственный способ убедиться в том, какие типы поддерживаются, — это проверить их, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="fe69f-130">The only way to know for certain which types are supported is to test them, as described in the next section.</span></span>

<span data-ttu-id="fe69f-131">**Установка типа мультимедиа в потоке**</span><span class="sxs-lookup"><span data-stu-id="fe69f-131">**Setting the Media Type on a Stream**</span></span>

<span data-ttu-id="fe69f-132">Используйте методы [**имедиаобжект:: сетинпуттипе**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) и [**Имедиаобжект:: сетаутпуттипе**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) , чтобы задать тип для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="fe69f-132">Use the [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) and [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) methods to set the type for each stream.</span></span> <span data-ttu-id="fe69f-133">Необходимо предоставить структуру **\_ \_ типа мультимедиа DMO** , содержащую полное описание типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fe69f-133">You must provide a **DMO\_MEDIA\_TYPE** structure that contains a complete description of the media type.</span></span> <span data-ttu-id="fe69f-134">В следующем примере задается тип мультимедиа в потоке входных данных 0 с использованием 16-разрядного стереозвука стерео 44,1-кГц:</span><span class="sxs-lookup"><span data-stu-id="fe69f-134">The following example sets the media type on input stream 0, using 44.1-kHz 16-bit stereo PCM audio:</span></span>


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="fe69f-135">Чтобы проверить тип мультимедиа, не настроив его, вызовите **сетинпуттипе** или **сетаутпуттипе** с \_ \_ флагом DMO Set типеф \_ только тестовый \_ .</span><span class="sxs-lookup"><span data-stu-id="fe69f-135">To test a media type without setting it, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_TEST\_ONLY flag.</span></span> <span data-ttu-id="fe69f-136">Метод возвращает значение S \_ , если тип приемлем, или \_ false в противном случае:</span><span class="sxs-lookup"><span data-stu-id="fe69f-136">The method returns S\_OK if the type is acceptable, or S\_FALSE otherwise:</span></span>


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



<span data-ttu-id="fe69f-137">Поскольку параметры одного потока могут повлиять на другой поток, может потребоваться очистить тип носителя потока.</span><span class="sxs-lookup"><span data-stu-id="fe69f-137">Because the settings on one stream can affect another stream, you might need to clear a stream's media type.</span></span> <span data-ttu-id="fe69f-138">Для этого вызовите **сетинпуттипе** или **СЕТАУТПУТТИПЕ** с помощью DMO \_ Set \_ типеф \_ clear флаг.</span><span class="sxs-lookup"><span data-stu-id="fe69f-138">To do this, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_CLEAR flag.</span></span>

<span data-ttu-id="fe69f-139">Для декодера DMO клиент, как правило, должен сначала задать входной тип, а затем выбрать тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fe69f-139">For a decoder DMO, the client would typically set the input type first, and then choose an output type.</span></span> <span data-ttu-id="fe69f-140">Для кодировщика DMO клиент должен сначала задать тип вывода, а затем тип входных данных.</span><span class="sxs-lookup"><span data-stu-id="fe69f-140">For an encoder DMO, the client would set the output type first, and then the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe69f-141">См. также</span><span class="sxs-lookup"><span data-stu-id="fe69f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe69f-142">Непосредственное размещение DMO</span><span class="sxs-lookup"><span data-stu-id="fe69f-142">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



