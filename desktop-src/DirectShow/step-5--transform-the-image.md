---
description: Используйте этот пример, чтобы понять, как кодировщик RLE может реализовать метод в процессе записи фильтра преобразования.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Шаг 5. Преобразование изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac9d32e48ba438f8bde2d8d4d9aca3b827ebc0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406787"
---
# <a name="step-5-transform-the-image"></a><span data-ttu-id="a13b5-104">Шаг 5.</span><span class="sxs-lookup"><span data-stu-id="a13b5-104">Step 5.</span></span> <span data-ttu-id="a13b5-105">Преобразование изображения</span><span class="sxs-lookup"><span data-stu-id="a13b5-105">Transform the Image</span></span>

<span data-ttu-id="a13b5-106">Это шаг 5 учебника [Создание фильтров преобразования](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="a13b5-106">This is step 5 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="a13b5-107">Вышестоящий фильтр доставляет примеры носителей в фильтр преобразования, вызывая метод [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) для входного ПИН-кода фильтра преобразования.</span><span class="sxs-lookup"><span data-stu-id="a13b5-107">The upstream filter delivers media samples to the transform filter by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the transform filter's input pin.</span></span> <span data-ttu-id="a13b5-108">Для обработки данных фильтр преобразования вызывает метод **Transform** , который является чистым виртуальным.</span><span class="sxs-lookup"><span data-stu-id="a13b5-108">To process the data, the transform filter calls the **Transform** method, which is pure virtual.</span></span> <span data-ttu-id="a13b5-109">Классы **ктрансформфилтер** и **ктрансинплацефилтер** используют две разные версии этого метода:</span><span class="sxs-lookup"><span data-stu-id="a13b5-109">The **CTransformFilter** and **CTransInPlaceFilter** classes use two different versions of this method:</span></span>

-   <span data-ttu-id="a13b5-110">[**Ктрансформфилтер:: Transform**](ctransformfilter-transform.md) принимает указатель на образец входных данных и указатель на образец Output.</span><span class="sxs-lookup"><span data-stu-id="a13b5-110">[**CTransformFilter::Transform**](ctransformfilter-transform.md) takes a pointer to the input sample and a pointer to the output sample.</span></span> <span data-ttu-id="a13b5-111">Перед тем как фильтр вызовет метод, он копирует примеры свойств из примера входных данных в образец Output, включая отметки времени.</span><span class="sxs-lookup"><span data-stu-id="a13b5-111">Before the filter calls the method, it copies the sample properties from the input sample to the output sample, including the time stamps.</span></span>
-   <span data-ttu-id="a13b5-112">[**Ктрансинплацефилтер:: Transform**](ctransinplacefilter-transform.md) принимает указатель на входной образец.</span><span class="sxs-lookup"><span data-stu-id="a13b5-112">[**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) takes a pointer to the input sample.</span></span> <span data-ttu-id="a13b5-113">Фильтр изменяет данные на месте.</span><span class="sxs-lookup"><span data-stu-id="a13b5-113">The filter modifies the data in place.</span></span>

<span data-ttu-id="a13b5-114">Если метод **Transform** возвращает значение S \_ , то фильтр доставляет пример нисходящий.</span><span class="sxs-lookup"><span data-stu-id="a13b5-114">If the **Transform** method returns S\_OK, the filter delivers the sample downstream.</span></span> <span data-ttu-id="a13b5-115">Чтобы пропустить кадр, возвратите \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="a13b5-115">To skip a frame, return S\_FALSE.</span></span> <span data-ttu-id="a13b5-116">При возникновении ошибки потоковой передачи возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="a13b5-116">If there is a streaming error, return a failure code.</span></span>

<span data-ttu-id="a13b5-117">В следующем примере показано, как кодировщик RLE может реализовать этот метод.</span><span class="sxs-lookup"><span data-stu-id="a13b5-117">The following example shows how the RLE encoder might implement this method.</span></span> <span data-ttu-id="a13b5-118">Ваша собственная реализация может значительно различаться в зависимости от того, что делает фильтр.</span><span class="sxs-lookup"><span data-stu-id="a13b5-118">Your own implementation might differ considerably, depending on what your filter does.</span></span>


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



<span data-ttu-id="a13b5-119">В этом примере предполагается, что Енкодефраме является частным методом, реализующим кодирование RLE.</span><span class="sxs-lookup"><span data-stu-id="a13b5-119">This example assumes that EncodeFrame is a private method that implements the RLE encoding.</span></span> <span data-ttu-id="a13b5-120">Сам алгоритм кодирования не описан здесь; Дополнительные сведения см. в разделе "Сжатие растрового изображения" в документации по Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="a13b5-120">The encoding algorithm itself is not described here; for details, see the topic "Bitmap Compression" in the Platform SDK documentation.</span></span>

<span data-ttu-id="a13b5-121">Сначала в примере вызывается [**имедиасампле:: "**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) , чтобы получить адреса базовых буферов.</span><span class="sxs-lookup"><span data-stu-id="a13b5-121">First, the example calls [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) to retrieve the addresses of the underlying buffers.</span></span> <span data-ttu-id="a13b5-122">Он передает их закрытому методу Енкодерфраме.</span><span class="sxs-lookup"><span data-stu-id="a13b5-122">It passes these to the private EncoderFrame method.</span></span> <span data-ttu-id="a13b5-123">Затем вызывается [**имедиасампле:: сетактуалдаталенгс**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) , чтобы указать длину закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="a13b5-123">Then it calls [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) to specify the length of the encoded data.</span></span> <span data-ttu-id="a13b5-124">Подчиненный фильтр требует этой информации, чтобы она могла правильно управлять буфером.</span><span class="sxs-lookup"><span data-stu-id="a13b5-124">The downstream filter needs this information so that it can manage the buffer properly.</span></span> <span data-ttu-id="a13b5-125">Наконец, метод вызывает [**имедиасампле:: сетсинкпоинт**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) , чтобы установить для флага ключевого кадра **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a13b5-125">Finally, the method calls [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) to set the key frame flag to **TRUE**.</span></span> <span data-ttu-id="a13b5-126">При кодировании с длиной не используются никакие разностные кадры, поэтому каждый кадр является ключевым кадром.</span><span class="sxs-lookup"><span data-stu-id="a13b5-126">Run-length encoding does not use any delta frames, so every frame is a key frame.</span></span> <span data-ttu-id="a13b5-127">Для разностных кадров установите значение **false**.</span><span class="sxs-lookup"><span data-stu-id="a13b5-127">For delta frames, set the value to **FALSE**.</span></span>

<span data-ttu-id="a13b5-128">Ниже приведены другие проблемы, которые необходимо учитывать.</span><span class="sxs-lookup"><span data-stu-id="a13b5-128">Other issues that you must consider include:</span></span>

-   <span data-ttu-id="a13b5-129">Метки времени.</span><span class="sxs-lookup"><span data-stu-id="a13b5-129">Time stamps.</span></span> <span data-ttu-id="a13b5-130">Класс **ктрансформфилтер** отметок времени для образца Output перед вызовом метода **Transform** .</span><span class="sxs-lookup"><span data-stu-id="a13b5-130">The **CTransformFilter** class timestamps the output sample before calling the **Transform** method.</span></span> <span data-ttu-id="a13b5-131">Он копирует значения временной метки из образца входных данных, не изменяя их.</span><span class="sxs-lookup"><span data-stu-id="a13b5-131">It copies the time stamp values from the input sample, without modifying them.</span></span> <span data-ttu-id="a13b5-132">Если фильтру необходимо изменить отметки времени, вызовите [**имедиасампле:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) в примере Output.</span><span class="sxs-lookup"><span data-stu-id="a13b5-132">If your filter needs to change the time stamps, call [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) on the output sample.</span></span>
-   <span data-ttu-id="a13b5-133">Изменения формата.</span><span class="sxs-lookup"><span data-stu-id="a13b5-133">Format changes.</span></span> <span data-ttu-id="a13b5-134">Вышестоящий фильтр может изменять форматы среднего потока, присоединяя к образцу тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a13b5-134">The upstream filter can change formats mid-stream by attaching a media type to the sample.</span></span> <span data-ttu-id="a13b5-135">Перед этим он вызывает [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) для входного ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="a13b5-135">Before doing so, it calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on your filter's input pin.</span></span> <span data-ttu-id="a13b5-136">В классе **ктрансформфилтер** это приводит к вызову **чеккинпуттипе** , за которым следует **чекктрансформ**.</span><span class="sxs-lookup"><span data-stu-id="a13b5-136">In the **CTransformFilter** class, this results in a call to **CheckInputType** followed by **CheckTransform**.</span></span> <span data-ttu-id="a13b5-137">Нисходящий фильтр также может изменять типы носителей, используя тот же механизм.</span><span class="sxs-lookup"><span data-stu-id="a13b5-137">The downstream filter can also change media types, using the same mechanism.</span></span> <span data-ttu-id="a13b5-138">В собственном фильтре необходимо обратить внимание на следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="a13b5-138">In your own filter, there are two things to watch for:</span></span>

    -   <span data-ttu-id="a13b5-139">Убедитесь, что **куерякцепт** не возвращает ложные приемы.</span><span class="sxs-lookup"><span data-stu-id="a13b5-139">Make sure that **QueryAccept** does not return false acceptances.</span></span>
    -   <span data-ttu-id="a13b5-140">Если фильтр принимает изменения формата, проверьте их внутри метода **Transform** , вызвав [**Имедиасампле:: жетмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="a13b5-140">If your filter does accept format changes, check for them inside the **Transform** method by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="a13b5-141">Если этот метод возвращает значение S \_ , то фильтр должен реагировать на изменение формата.</span><span class="sxs-lookup"><span data-stu-id="a13b5-141">If that method returns S\_OK, your filter must respond to the format change.</span></span>

    <span data-ttu-id="a13b5-142">Дополнительные сведения см. в разделе [динамические изменения формата](dynamic-format-changes.md).</span><span class="sxs-lookup"><span data-stu-id="a13b5-142">For more information, see [Dynamic Format Changes](dynamic-format-changes.md).</span></span>

-   <span data-ttu-id="a13b5-143">Многопоточно.</span><span class="sxs-lookup"><span data-stu-id="a13b5-143">Threads.</span></span> <span data-ttu-id="a13b5-144">В **ктрансформфилтер** и **ктрансинплацефилтер** фильтр преобразования доставляет выходные примеры синхронно внутри метода **Receive** .</span><span class="sxs-lookup"><span data-stu-id="a13b5-144">In both **CTransformFilter** and **CTransInPlaceFilter**, the transform filter delivers output samples synchronously inside the **Receive** method.</span></span> <span data-ttu-id="a13b5-145">Фильтр не создает рабочие потоки для обработки данных.</span><span class="sxs-lookup"><span data-stu-id="a13b5-145">The filter does not create any worker threads to process the data.</span></span> <span data-ttu-id="a13b5-146">Как правило, для фильтра преобразований нет причин создавать рабочие потоки.</span><span class="sxs-lookup"><span data-stu-id="a13b5-146">Typically, there is no reason for a transform filter to create worker threads.</span></span>

<span data-ttu-id="a13b5-147">Далее. [Шаг 6. Добавлена поддержка COM](step-6--add-support-for-com.md).</span><span class="sxs-lookup"><span data-stu-id="a13b5-147">Next: [Step 6. Add Support for COM](step-6--add-support-for-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a13b5-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a13b5-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a13b5-149">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="a13b5-149">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



