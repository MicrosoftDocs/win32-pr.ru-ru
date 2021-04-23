---
description: В этом разделе приведен подробный обзор примера пакета SDK MPEG-1 Media Source.
ms.assetid: d392f30c-c963-4eb3-add2-1bb986919c0b
title: 'Пример использования: источник мультимедиа MPEG-1'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e1f72cc6ae6df119439bdae1942732bf8d2fa2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104081686"
---
# <a name="case-study-mpeg-1-media-source"></a><span data-ttu-id="49216-103">Пример использования: источник мультимедиа MPEG-1</span><span class="sxs-lookup"><span data-stu-id="49216-103">Case Study: MPEG-1 Media Source</span></span>

<span data-ttu-id="49216-104">В Microsoft Media Foundation объект, который представляет данные мультимедиа в конвейере данных, называется *источником мультимедиа*.</span><span class="sxs-lookup"><span data-stu-id="49216-104">In Microsoft Media Foundation, the object that introduces media data into the data pipeline is called a *media source*.</span></span> <span data-ttu-id="49216-105">В этом разделе приведен подробный обзор примера пакета SDK [MPEG-1 Media Source](mpeg1source-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-105">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span>

-   [<span data-ttu-id="49216-106">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="49216-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="49216-107">Классы C++, используемые в источнике MPEG-1</span><span class="sxs-lookup"><span data-stu-id="49216-107">C++ Classes Used in the MPEG-1 Source</span></span>](#c-classes-used-in-the-mpeg-1-source)
-   [<span data-ttu-id="49216-108">Обработчик потока байтов</span><span class="sxs-lookup"><span data-stu-id="49216-108">Byte-Stream Handler</span></span>](#byte-stream-handler)
-   [<span data-ttu-id="49216-109">Дескриптор представления</span><span class="sxs-lookup"><span data-stu-id="49216-109">Presentation Descriptor</span></span>](#presentation-descriptor)
-   [<span data-ttu-id="49216-110">Состояния потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="49216-110">Streaming States</span></span>](#streaming-states)
    -   [<span data-ttu-id="49216-111">Запуск</span><span class="sxs-lookup"><span data-stu-id="49216-111">Start</span></span>](#start)
    -   [<span data-ttu-id="49216-112">Пауза</span><span class="sxs-lookup"><span data-stu-id="49216-112">Pause</span></span>](#pause)
    -   [<span data-ttu-id="49216-113">Остановить</span><span class="sxs-lookup"><span data-stu-id="49216-113">Stop</span></span>](#stop)
-   [<span data-ttu-id="49216-114">Примеры запросов</span><span class="sxs-lookup"><span data-stu-id="49216-114">Sample Requests</span></span>](#sample-requests)
-   [<span data-ttu-id="49216-115">Конец потока</span><span class="sxs-lookup"><span data-stu-id="49216-115">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="49216-116">Асинхронные операции</span><span class="sxs-lookup"><span data-stu-id="49216-116">Asynchronous Operations</span></span>](#asynchronous-operations)
    -   [<span data-ttu-id="49216-117">Очередь операций</span><span class="sxs-lookup"><span data-stu-id="49216-117">Operation Queue</span></span>](#operation-queue)
-   [<span data-ttu-id="49216-118">См. также</span><span class="sxs-lookup"><span data-stu-id="49216-118">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="49216-119">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="49216-119">Prerequisites</span></span>

<span data-ttu-id="49216-120">Прежде чем читать этот раздел, необходимо ознакомиться со следующими концепциями Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="49216-120">Before reading this topic you should understand the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="49216-121">Объектная модель источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="49216-121">Media Source Object Model</span></span>](media-source-object-model.md)
-   <span data-ttu-id="49216-122">[Асинхронные методы обратного вызова](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="49216-122">[Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>
-   [<span data-ttu-id="49216-123">Рабочие очереди</span><span class="sxs-lookup"><span data-stu-id="49216-123">Work Queues</span></span>](work-queues.md)
-   [<span data-ttu-id="49216-124">Генераторы событий мультимедиа</span><span class="sxs-lookup"><span data-stu-id="49216-124">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="49216-125">Буферы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="49216-125">Media Buffers</span></span>](media-buffers.md)
-   [<span data-ttu-id="49216-126">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="49216-126">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="49216-127">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="49216-127">Media Types</span></span>](media-types.md)

<span data-ttu-id="49216-128">Кроме того, необходимо иметь базовое представление об архитектуре Media Foundation, в частности роль источников мультимедиа в конвейере.</span><span class="sxs-lookup"><span data-stu-id="49216-128">You should also have a basic understanding of the Media Foundation architecture, particularly the role of media sources in the pipeline.</span></span> <span data-ttu-id="49216-129">(Дополнительные сведения см. в разделе [источники мультимедиа](media-sources.md).)</span><span class="sxs-lookup"><span data-stu-id="49216-129">(For more information, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="49216-130">Кроме того, может потребоваться ознакомиться с разделом [Создание пользовательского источника мультимедиа](writing-a-custom-media-source.md), в котором приводятся более общие сведения о действиях, описанных здесь.</span><span class="sxs-lookup"><span data-stu-id="49216-130">In addition, you may want to read the topic [Writing a Custom Media Source](writing-a-custom-media-source.md), which gives a more general overview of the steps described here.</span></span>

<span data-ttu-id="49216-131">Этот раздел не позволяет воспроизвести весь код из примера пакета SDK, так как этот пример довольно большой.</span><span class="sxs-lookup"><span data-stu-id="49216-131">This topic does not reproduce all of the code from the SDK sample, because the sample is fairly large.</span></span>

## <a name="c-classes-used-in-the-mpeg-1-source"></a><span data-ttu-id="49216-132">Классы C++, используемые в источнике MPEG-1</span><span class="sxs-lookup"><span data-stu-id="49216-132">C++ Classes Used in the MPEG-1 Source</span></span>

<span data-ttu-id="49216-133">Образец источника MPEG-1 реализуется со следующими классами C++:</span><span class="sxs-lookup"><span data-stu-id="49216-133">The sample MPEG-1 source is implemented with the following C++ classes:</span></span>

-   <span data-ttu-id="49216-134">`MPEG1ByteStreamHandler`.</span><span class="sxs-lookup"><span data-stu-id="49216-134">`MPEG1ByteStreamHandler`.</span></span> <span data-ttu-id="49216-135">Реализует обработчик потока байтов для источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-135">Implements the byte-stream handler for the media source.</span></span> <span data-ttu-id="49216-136">При наличии потока байтов обработчик потока байтов создает экземпляр источника.</span><span class="sxs-lookup"><span data-stu-id="49216-136">Given a byte stream, the byte-stream handler creates an instance of the source.</span></span>
-   <span data-ttu-id="49216-137">`MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="49216-137">`MPEG1Source`.</span></span> <span data-ttu-id="49216-138">Реализует источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-138">Implements the media source.</span></span>
-   <span data-ttu-id="49216-139">`MPEG1Stream`.</span><span class="sxs-lookup"><span data-stu-id="49216-139">`MPEG1Stream`.</span></span> <span data-ttu-id="49216-140">Реализует объекты потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-140">Implements the media stream objects.</span></span> <span data-ttu-id="49216-141">Источник мультимедиа создает по одному `MPEG1Stream` объекту для каждого звукового или видеопотока в формате MPEG-1 битовый поток.</span><span class="sxs-lookup"><span data-stu-id="49216-141">The media source creates one `MPEG1Stream` object for every audio or video stream in the MPEG-1 bitstream.</span></span>
-   <span data-ttu-id="49216-142">`Parser`.</span><span class="sxs-lookup"><span data-stu-id="49216-142">`Parser`.</span></span> <span data-ttu-id="49216-143">Выполняет синтаксический анализ битовый поток MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="49216-143">Parses the MPEG-1 bitstream.</span></span> <span data-ttu-id="49216-144">В большинстве случаев сведения этого класса не относятся к Media Foundationным API.</span><span class="sxs-lookup"><span data-stu-id="49216-144">For the most part, the details of this class are not relevant to the Media Foundation APIs.</span></span>
-   <span data-ttu-id="49216-145">Саурцеоп, Опкуеуе. Эти два класса управляют асинхронными операциями в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-145">SourceOp, OpQueue: These two classes manage asynchronous operations in the media source.</span></span> <span data-ttu-id="49216-146">(См. раздел [асинхронные операции](#asynchronous-operations)).</span><span class="sxs-lookup"><span data-stu-id="49216-146">(See [Asynchronous Operations](#asynchronous-operations)).</span></span>

<span data-ttu-id="49216-147">Другие вспомогательные классы описаны далее в разделе.</span><span class="sxs-lookup"><span data-stu-id="49216-147">Other miscellaneous helper classes are described later in the topic.</span></span>

## <a name="byte-stream-handler"></a><span data-ttu-id="49216-148">Обработчик Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="49216-148">Byte-Stream Handler</span></span>

<span data-ttu-id="49216-149">Обработчик *байтов потока* — это объект, который создает источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-149">The *byte-stream* handler is the object that creates the media source.</span></span> <span data-ttu-id="49216-150">Обработчик потока байтов создается исходным распознавателем. приложения не взаимодействуют напрямую с обработчиком потока байтов.</span><span class="sxs-lookup"><span data-stu-id="49216-150">The byte-stream handler is created by the source resolver; applications do not interact directly with the byte-stream handler.</span></span> <span data-ttu-id="49216-151">Сопоставитель источника обнаруживает обработчик потока байтов, просматривая в реестре.</span><span class="sxs-lookup"><span data-stu-id="49216-151">The source resolver discovers the byte-stream handler by looking in the registry.</span></span> <span data-ttu-id="49216-152">Обработчик регистрируется по расширению имени файла или типу MIME.</span><span class="sxs-lookup"><span data-stu-id="49216-152">Handler are registered by file name extension or MIME type.</span></span> <span data-ttu-id="49216-153">Для источника MPEG-1 обработчик потока байтов регистрируется для расширения имени файла ". mpg".</span><span class="sxs-lookup"><span data-stu-id="49216-153">For the MPEG-1 source, the byte-stream handler is registered for the ".mpg" file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="49216-154">Если требуется поддержка пользовательских схем URL-адресов, можно также написать *обработчик схемы*.</span><span class="sxs-lookup"><span data-stu-id="49216-154">If you want to support custom URL schemes, you can also write a *scheme handler*.</span></span> <span data-ttu-id="49216-155">Источник MPEG-1 предназначен для локальных файлов, а Media Foundation уже предоставляет обработчик схемы для URL-адресов "file://".</span><span class="sxs-lookup"><span data-stu-id="49216-155">The MPEG-1 source is designed for local files, and Media Foundation already provides a scheme handler for "file://" URLs.</span></span>

 

<span data-ttu-id="49216-156">Обработчик потока байтов реализует интерфейс [**имфбитестреамхандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="49216-156">The byte-stream handler implements the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="49216-157">Этот интерфейс имеет два наиболее важных метода, которые должны быть реализованы:</span><span class="sxs-lookup"><span data-stu-id="49216-157">This interface has two most important methods that must be implemented:</span></span>

-   <span data-ttu-id="49216-158">[**Бегинкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span><span class="sxs-lookup"><span data-stu-id="49216-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="49216-159">Запускает асинхронную операцию для создания источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-159">Starts an asynchronous operation to create the media source.</span></span>
-   <span data-ttu-id="49216-160">[**Ендкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span><span class="sxs-lookup"><span data-stu-id="49216-160">[**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="49216-161">Завершает асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="49216-161">Completes the asynchronous call.</span></span>

<span data-ttu-id="49216-162">Два других метода являются необязательными и не реализуются в примере пакета SDK:</span><span class="sxs-lookup"><span data-stu-id="49216-162">Two other methods are optional and not implemented in the SDK sample:</span></span>

-   <span data-ttu-id="49216-163">[**Канцелобжекткреатион**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span><span class="sxs-lookup"><span data-stu-id="49216-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span></span> <span data-ttu-id="49216-164">Отменяет метод [**бегинкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) .</span><span class="sxs-lookup"><span data-stu-id="49216-164">Cancels the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method.</span></span> <span data-ttu-id="49216-165">Этот метод полезен для сетевого источника, который может иметь высокую задержку при запуске.</span><span class="sxs-lookup"><span data-stu-id="49216-165">This method is useful for a network source that might have a high latency at startup.</span></span>
-   <span data-ttu-id="49216-166">[**Жетмакснумберофбитесрекуиредфорресолутион**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span><span class="sxs-lookup"><span data-stu-id="49216-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span></span> <span data-ttu-id="49216-167">Возвращает максимальное число байтов, которое обработчик будет считывать из исходного потока.</span><span class="sxs-lookup"><span data-stu-id="49216-167">Gets the maximum number of bytes that the handler will read from the source stream.</span></span> <span data-ttu-id="49216-168">Реализуйте этот метод, если известно, сколько данных обработчика потока байтов перед созданием источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-168">Implement this method if you know how much data the byte-stream handler before it can create the media source.</span></span> <span data-ttu-id="49216-169">В противном случае просто возвратите **E \_ нотимпл**.</span><span class="sxs-lookup"><span data-stu-id="49216-169">Otherwise, simply return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="49216-170">Ниже приведена реализация метода [**бегинкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) :</span><span class="sxs-lookup"><span data-stu-id="49216-170">Here is the implementation of the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method:</span></span>


```C++
HRESULT MPEG1ByteStreamHandler::BeginCreateObject(
        /* [in] */ IMFByteStream *pByteStream,
        /* [in] */ LPCWSTR pwszURL,
        /* [in] */ DWORD dwFlags,
        /* [in] */ IPropertyStore *pProps,
        /* [out] */ IUnknown **ppIUnknownCancelCookie,  // Can be NULL
        /* [in] */ IMFAsyncCallback *pCallback,
        /* [in] */ IUnknown *punkState                  // Can be NULL
        )
{
    if (pByteStream == NULL)
    {
        return E_POINTER;
    }

    if (pCallback == NULL)
    {
        return E_POINTER;
    }

    if ((dwFlags & MF_RESOLUTION_MEDIASOURCE) == 0)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFAsyncResult *pResult = NULL;
    MPEG1Source    *pSource = NULL;

    // Create an instance of the media source.
    hr = MPEG1Source::CreateInstance(&pSource);

    // Create a result object for the caller's async callback.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);
    }

    // Start opening the source. This is an async operation.
    // When it completes, the source will invoke our callback
    // and then we will invoke the caller's callback.
    if (SUCCEEDED(hr))
    {
        hr = pSource->BeginOpen(pByteStream, this, NULL);
    }

    if (SUCCEEDED(hr))
    {
        if (ppIUnknownCancelCookie)
        {
            *ppIUnknownCancelCookie = NULL;
        }

        m_pSource = pSource;
        m_pSource->AddRef();

        m_pResult = pResult;
        m_pResult->AddRef();
    }

// cleanup
    SafeRelease(&pSource);
    SafeRelease(&pResult);
    return hr;
}
```



<span data-ttu-id="49216-171">Метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="49216-171">The method performs the following steps:</span></span>

1.  <span data-ttu-id="49216-172">Создает новый экземпляр объекта `MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="49216-172">Creates a new instance of the `MPEG1Source` object.</span></span>
2.  <span data-ttu-id="49216-173">Создайте объект асинхронного результата.</span><span class="sxs-lookup"><span data-stu-id="49216-173">Create an asynchronous result object.</span></span> <span data-ttu-id="49216-174">Этот объект используется позже для вызова метода обратного вызова распознавателя источника.</span><span class="sxs-lookup"><span data-stu-id="49216-174">This object is used later to invoke the source resolver's callback method.</span></span>
3.  <span data-ttu-id="49216-175">Вызывает `MPEG1Source::BeginOpen` асинхронный метод, определенный в `MPEG1Source` классе.</span><span class="sxs-lookup"><span data-stu-id="49216-175">Calls `MPEG1Source::BeginOpen`, an asynchronous method defined in the `MPEG1Source` class.</span></span>
4.  <span data-ttu-id="49216-176">Устанавливает *ппиункновнканцелкукие* в **значение NULL**, которое информирует вызывающий объект о том, что [**канцелобжекткреатион**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="49216-176">Sets *ppIUnknownCancelCookie* to **NULL**, which informs the caller that [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) is not supported.</span></span>

<span data-ttu-id="49216-177">`MPEG1Source::BeginOpen`Метод выполняет фактическую работу по чтению потока байтов и инициализации `MPEG1Source` объекта.</span><span class="sxs-lookup"><span data-stu-id="49216-177">The `MPEG1Source::BeginOpen` method does the actual work of reading the byte stream and initializing the `MPEG1Source` object.</span></span> <span data-ttu-id="49216-178">Этот метод не является частью общедоступного API.</span><span class="sxs-lookup"><span data-stu-id="49216-178">This method is not part of the public API.</span></span> <span data-ttu-id="49216-179">Можно определить любой механизм между обработчиком и источником мультимедиа, отвечающим вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="49216-179">You can define any mechanism between the handler and the media source that suits your needs.</span></span> <span data-ttu-id="49216-180">Размещение большей части логики в источнике мультимедиа обеспечивает сравнительно простой обработчик потока байтов.</span><span class="sxs-lookup"><span data-stu-id="49216-180">Putting most of the logic into the media source keeps the byte-stream handler relatively simple.</span></span>

<span data-ttu-id="49216-181">Вкратце, `BeginOpen` выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="49216-181">Briefly, `BeginOpen` does the following:</span></span>

1.  <span data-ttu-id="49216-182">Вызывает [**имфбитестреам::-Capabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) , чтобы убедиться, что исходный байтовый поток доступен для чтения и поиска.</span><span class="sxs-lookup"><span data-stu-id="49216-182">Calls [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) to verify that the source byte stream is both readable and seekable.</span></span>
2.  <span data-ttu-id="49216-183">Вызывает метод [**имфбитестреам:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) для запуска асинхронного запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="49216-183">Calls [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) to start an asynchronous I/O request.</span></span>

<span data-ttu-id="49216-184">Остальная часть инициализации выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="49216-184">The rest of the initialization occurs asynchronously.</span></span> <span data-ttu-id="49216-185">Источник мультимедиа считывает из потока достаточно данных для синтаксического анализа заголовков последовательности MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="49216-185">The media source reads enough data from the stream to parse the MPEG-1 sequence headers.</span></span> <span data-ttu-id="49216-186">Затем создается *дескриптор представления*, который является объектом, используемым для описания потоков аудио и видео в файле.</span><span class="sxs-lookup"><span data-stu-id="49216-186">Then it creates a *presentation descriptor*, which is the object used to describe the audio and video streams in the file.</span></span> <span data-ttu-id="49216-187">(Дополнительные сведения см. в разделе [дескриптор представления](#presentation-descriptor).) По `BeginOpen` завершении операции обработчик потока байтов вызывает метод обратного вызова распознавателя исходного кода.</span><span class="sxs-lookup"><span data-stu-id="49216-187">(For more information, see [Presentation Descriptor](#presentation-descriptor).) When the `BeginOpen` operation completes, the byte-stream handler invokes the source resolver's callback method.</span></span> <span data-ttu-id="49216-188">На этом этапе сопоставитель источника вызывает [**имфбитестреамхандлер:: ендкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span><span class="sxs-lookup"><span data-stu-id="49216-188">At that point, the source resolver calls [**IMFByteStreamHandler::EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="49216-189">Метод **ендкреатеобжект** возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="49216-189">The **EndCreateObject** method returns the status of the operation.</span></span>


```C++
HRESULT MPEG1ByteStreamHandler::EndCreateObject(
        /* [in] */ IMFAsyncResult *pResult,
        /* [out] */ MF_OBJECT_TYPE *pObjectType,
        /* [out] */ IUnknown **ppObject)
{
    if (pResult == NULL || pObjectType == NULL || ppObject == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    *pObjectType = MF_OBJECT_INVALID;
    *ppObject = NULL;

    hr = pResult->GetStatus();

    if (SUCCEEDED(hr))
    {
        *pObjectType = MF_OBJECT_MEDIASOURCE;

        assert(m_pSource != NULL);

        hr = m_pSource->QueryInterface(IID_PPV_ARGS(ppObject));
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pResult);
    return hr;
}
```



<span data-ttu-id="49216-190">Если во время этого процесса возникает ошибка, обратный вызов вызывается с кодом состояния ошибки.</span><span class="sxs-lookup"><span data-stu-id="49216-190">If an error occurs at any time during this process, the callback is invoked with an error status code.</span></span>

## <a name="presentation-descriptor"></a><span data-ttu-id="49216-191">Дескриптор представления</span><span class="sxs-lookup"><span data-stu-id="49216-191">Presentation Descriptor</span></span>

<span data-ttu-id="49216-192">Дескриптор презентации описывает содержимое файла MPEG-1, включая следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="49216-192">The presentation descriptor describes the contents of the MPEG-1 file, including the following information:</span></span>

-   <span data-ttu-id="49216-193">Число потоков.</span><span class="sxs-lookup"><span data-stu-id="49216-193">The number of the streams.</span></span>
-   <span data-ttu-id="49216-194">Формат каждого потока.</span><span class="sxs-lookup"><span data-stu-id="49216-194">The format of each stream.</span></span>
-   <span data-ttu-id="49216-195">Идентификаторы потоков.</span><span class="sxs-lookup"><span data-stu-id="49216-195">Stream identifiers.</span></span>
-   <span data-ttu-id="49216-196">Состояние выбора каждого потока (выбрано или отменяется выбор).</span><span class="sxs-lookup"><span data-stu-id="49216-196">The selection status of each stream (selected or deselected).</span></span>

<span data-ttu-id="49216-197">В терминах архитектуры Media Foundation дескриптор презентации содержит один или несколько *дескрипторов потоков*.</span><span class="sxs-lookup"><span data-stu-id="49216-197">In terms of the Media Foundation architecture, the presentation descriptor contains one or more *stream descriptors*.</span></span> <span data-ttu-id="49216-198">Каждый дескриптор потока содержит *обработчик типа мультимедиа*, который используется для получения или задания типов мультимедиа в потоке.</span><span class="sxs-lookup"><span data-stu-id="49216-198">Each stream descriptor contains a *media type handler*, which is used to get or set media types on the stream.</span></span> <span data-ttu-id="49216-199">Media Foundation предоставляет стандартные реализации дескриптора презентации и дескриптора потока; они подходят для большинства источников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-199">Media Foundation provides stock implementations for the presentation descriptor and stream descriptor; these are suitable for most media sources.</span></span>

<span data-ttu-id="49216-200">Чтобы создать дескриптор презентации, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="49216-200">To create a presentation descriptor, perform the following steps:</span></span>

1.  <span data-ttu-id="49216-201">Для каждого потока:</span><span class="sxs-lookup"><span data-stu-id="49216-201">For each stream:</span></span>
    1.  <span data-ttu-id="49216-202">Укажите идентификатор потока и массив возможных типов носителей.</span><span class="sxs-lookup"><span data-stu-id="49216-202">Provide a stream ID and an array of possible media types.</span></span> <span data-ttu-id="49216-203">Если поток поддерживает несколько типов носителей, упорядочивайте список типов мультимедиа по предпочтениям, если они есть.</span><span class="sxs-lookup"><span data-stu-id="49216-203">If the stream supports more than one media type, order the list of media types by preference, if any.</span></span> <span data-ttu-id="49216-204">(Сначала укажите оптимальный тип, а последний — самый оптимальный тип.)</span><span class="sxs-lookup"><span data-stu-id="49216-204">(Put the optimal type first, and the least optimal type last.)</span></span>
    2.  <span data-ttu-id="49216-205">Вызовите [**мфкреатестреамдескриптор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) , чтобы создать дескриптор потока.</span><span class="sxs-lookup"><span data-stu-id="49216-205">Call [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) to create the stream descriptor.</span></span>
    3.  <span data-ttu-id="49216-206">Вызовите [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) для только что созданного дескриптора потока.</span><span class="sxs-lookup"><span data-stu-id="49216-206">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the newly created stream descriptor.</span></span>
    4.  <span data-ttu-id="49216-207">Вызовите метод [**имфмедиатипехандлер:: сеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , чтобы задать формат по умолчанию для потока.</span><span class="sxs-lookup"><span data-stu-id="49216-207">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the default format for the stream.</span></span> <span data-ttu-id="49216-208">Если имеется более одного типа мультимедиа, обычно следует задать первый тип в списке.</span><span class="sxs-lookup"><span data-stu-id="49216-208">If there is more than one media type, you should generally set the first type in the list.</span></span>
2.  <span data-ttu-id="49216-209">Вызовите [**мфкреатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) и передайте массив указателей дескриптора потока.</span><span class="sxs-lookup"><span data-stu-id="49216-209">Call [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) and pass in the array of stream descriptor pointers.</span></span>
3.  <span data-ttu-id="49216-210">Для каждого потока вызовите [**имфпресентатиондескриптор:: селектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) или [**деселектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) , чтобы задать состояние выбора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49216-210">For each stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) or [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) to set the default selection state.</span></span> <span data-ttu-id="49216-211">Если имеется более одного потока одного типа (аудио или видео), по умолчанию должен быть выбран только один поток.</span><span class="sxs-lookup"><span data-stu-id="49216-211">If there is more than one stream of the same type (audio or video), only one should be selected by default.</span></span>

<span data-ttu-id="49216-212">`MPEG1Source`Объект создает дескриптор представления в своем `InitPresentationDescriptor` методе:</span><span class="sxs-lookup"><span data-stu-id="49216-212">The `MPEG1Source` object creates the presentation descriptor in its `InitPresentationDescriptor` method:</span></span>


```C++
HRESULT MPEG1Source::InitPresentationDescriptor()
{
    HRESULT hr = S_OK;
    DWORD cStreams = 0;

    assert(m_pPresentationDescriptor == NULL);
    assert(m_state == STATE_OPENING);

    if (m_pHeader == NULL)
    {
        return E_FAIL;
    }

    // Get the number of streams, as declared in the MPEG-1 header, skipping
    // any streams with an unsupported format.
    for (DWORD i = 0; i < m_pHeader->cStreams; i++)
    {
        if (IsStreamTypeSupported(m_pHeader->streams[i].type))
        {
            cStreams++;
        }
    }

    // How many streams do we actually have?
    if (cStreams > m_streams.GetCount())
    {
        // Keep reading data until we have seen a packet for each stream.
        return S_OK;
    }

    // We should never create a stream we don't support.
    assert(cStreams == m_streams.GetCount());

    // Ready to create the presentation descriptor.

    // Create an array of IMFStreamDescriptor pointers.
    IMFStreamDescriptor **ppSD =
            new (std::nothrow) IMFStreamDescriptor*[cStreams];

    if (ppSD == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    ZeroMemory(ppSD, cStreams * sizeof(IMFStreamDescriptor*));

    // Fill the array by getting the stream descriptors from the streams.
    for (DWORD i = 0; i < cStreams; i++)
    {
        hr = m_streams[i]->GetStreamDescriptor(&ppSD[i]);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the presentation descriptor.
    hr = MFCreatePresentationDescriptor(cStreams, ppSD,
        &m_pPresentationDescriptor);

    if (FAILED(hr))
    {
        goto done;
    }

    // Select the first video stream (if any).
    for (DWORD i = 0; i < cStreams; i++)
    {
        GUID majorType = GUID_NULL;

        hr = GetStreamMajorType(ppSD[i], &majorType);
        if (FAILED(hr))
        {
            goto done;
        }

        if (majorType == MFMediaType_Video)
        {
            hr = m_pPresentationDescriptor->SelectStream(i);
            if (FAILED(hr))
            {
                goto done;
            }
            break;
        }
    }

    // Switch state from "opening" to stopped.
    m_state = STATE_STOPPED;

    // Invoke the async callback to complete the BeginOpen operation.
    hr = CompleteOpen(S_OK);

done:
    // clean up:
    if (ppSD)
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            SafeRelease(&ppSD[i]);
        }
        delete [] ppSD;
    }
    return hr;
}
```



<span data-ttu-id="49216-213">Приложение получает дескриптор представления путем вызова [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="49216-213">The application gets the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="49216-214">Этот метод создает неполную копию дескриптора представления путем вызова [**имфпресентатиондескриптор:: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span><span class="sxs-lookup"><span data-stu-id="49216-214">This method creates a shallow copy of the presentation descriptor by calling [**IMFPresentationDescriptor::Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span></span> <span data-ttu-id="49216-215">(Копия содержит указатели на исходные дескрипторы потока.) Приложение может использовать дескриптор презентации, чтобы задать тип мультимедиа, выбрать поток или отменить выбор потока.</span><span class="sxs-lookup"><span data-stu-id="49216-215">(The copy contains pointers to the original stream descriptors.) The application can use the presentation descriptor to set the media type, select a stream, or deselect a stream.</span></span>

<span data-ttu-id="49216-216">При необходимости дескрипторы представления и дескрипторы потоков могут содержать атрибуты, предоставляющие дополнительные сведения об источнике.</span><span class="sxs-lookup"><span data-stu-id="49216-216">Optionally, presentation descriptors and stream descriptors can contain attributes that give additional information about the source.</span></span> <span data-ttu-id="49216-217">Список таких атрибутов см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="49216-217">For a list such attributes, see the following topics:</span></span>

-   [<span data-ttu-id="49216-218">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="49216-218">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
-   [<span data-ttu-id="49216-219">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="49216-219">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)

<span data-ttu-id="49216-220">Один атрибут заслуживает особого упоминания: атрибут [**« \_ \_ Длительность MF PD**](mf-pd-duration-attribute.md) » содержит общую длительность источника.</span><span class="sxs-lookup"><span data-stu-id="49216-220">One attribute deserves special mention: The [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute contains the total duration of the source.</span></span> <span data-ttu-id="49216-221">Установите этот атрибут, если вы уверены, что длительность находится впереди. Например, длительность может быть указана в заголовках файлов в зависимости от формата файла.</span><span class="sxs-lookup"><span data-stu-id="49216-221">Set this attribute if you know the duration up front; for example, the duration might be specified in the file headers, depending on the file format.</span></span> <span data-ttu-id="49216-222">Приложение может отобразить это значение или использовать его для задания индикатора выполнения или панели поиска.</span><span class="sxs-lookup"><span data-stu-id="49216-222">The application might display this value, or use it to set a progress bar or seek bar.</span></span>

## <a name="streaming-states"></a><span data-ttu-id="49216-223">Состояния потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="49216-223">Streaming States</span></span>

<span data-ttu-id="49216-224">Источник мультимедиа определяет следующие состояния.</span><span class="sxs-lookup"><span data-stu-id="49216-224">A media source defines the following states:</span></span>



| <span data-ttu-id="49216-225">Состояние</span><span class="sxs-lookup"><span data-stu-id="49216-225">State</span></span>    | <span data-ttu-id="49216-226">Описание</span><span class="sxs-lookup"><span data-stu-id="49216-226">Description</span></span>                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49216-227">Запуск</span><span class="sxs-lookup"><span data-stu-id="49216-227">Started</span></span>  | <span data-ttu-id="49216-228">Источник принимает и обрабатывает примеры запросов.</span><span class="sxs-lookup"><span data-stu-id="49216-228">The source accepts and processes sample requests.</span></span>                                                               |
| <span data-ttu-id="49216-229">Пауза</span><span class="sxs-lookup"><span data-stu-id="49216-229">Paused</span></span>   | <span data-ttu-id="49216-230">Источник принимает запросы выборки, но не обрабатывает их.</span><span class="sxs-lookup"><span data-stu-id="49216-230">The source accepts sample requests, but does not process them.</span></span> <span data-ttu-id="49216-231">Запросы ставятся в очередь до запуска источника.</span><span class="sxs-lookup"><span data-stu-id="49216-231">Requests are queued until the source is started.</span></span> |
| <span data-ttu-id="49216-232">Остановлена.</span><span class="sxs-lookup"><span data-stu-id="49216-232">Stopped.</span></span> | <span data-ttu-id="49216-233">Источник отклоняет запросы выборки.</span><span class="sxs-lookup"><span data-stu-id="49216-233">The source rejects sample requests.</span></span>                                                                             |



 

### <a name="start"></a><span data-ttu-id="49216-234">Начать</span><span class="sxs-lookup"><span data-stu-id="49216-234">Start</span></span>

<span data-ttu-id="49216-235">Метод [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) запускает источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-235">The [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method starts the media source.</span></span> <span data-ttu-id="49216-236">Она принимает следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="49216-236">It takes the following parameters:</span></span>

-   <span data-ttu-id="49216-237">Дескриптор презентации.</span><span class="sxs-lookup"><span data-stu-id="49216-237">A presentation descriptor.</span></span>
-   <span data-ttu-id="49216-238">Идентификатор GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="49216-238">A time-format GUID.</span></span>
-   <span data-ttu-id="49216-239">Начальное расположение.</span><span class="sxs-lookup"><span data-stu-id="49216-239">A start position.</span></span>

<span data-ttu-id="49216-240">Приложение должно получить дескриптор презентации, вызвав [**креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) в источнике.</span><span class="sxs-lookup"><span data-stu-id="49216-240">The application must obtain the presentation descriptor by calling [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) on the source.</span></span> <span data-ttu-id="49216-241">Нет определенного механизма для проверки дескриптора представления.</span><span class="sxs-lookup"><span data-stu-id="49216-241">There is no defined mechanism for validating a presentation descriptor.</span></span> <span data-ttu-id="49216-242">Если в приложении указан неправильный дескриптор представления, результаты не будут определены.</span><span class="sxs-lookup"><span data-stu-id="49216-242">If the application specifies the wrong presentation descriptor, the results are undefined.</span></span>

<span data-ttu-id="49216-243">Идентификатор GUID формата времени определяет способ интерпретации начальной должности.</span><span class="sxs-lookup"><span data-stu-id="49216-243">The time-format GUID specifies how to interpret the starting position.</span></span> <span data-ttu-id="49216-244">Стандартный формат — 100-наносекундных единиц (NS), обозначенный GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="49216-244">The standard format is 100-nanosecond (ns) units, indicated by GUID\_NULL.</span></span> <span data-ttu-id="49216-245">Каждый источник мультимедиа должен поддерживать 100-НС единиц.</span><span class="sxs-lookup"><span data-stu-id="49216-245">Every media source must support 100-ns units.</span></span> <span data-ttu-id="49216-246">Кроме того, источник может поддерживать другие единицы времени, такие как номер кадра или код времени.</span><span class="sxs-lookup"><span data-stu-id="49216-246">Optionally, a source can support other units of time, such as frame number or time code.</span></span> <span data-ttu-id="49216-247">Однако нет стандартного способа запросить источник мультимедиа список поддерживаемых форматов времени.</span><span class="sxs-lookup"><span data-stu-id="49216-247">However, there is no standard way to query a media source for the list of time formats it supports.</span></span>

<span data-ttu-id="49216-248">Начальное расположение задается как **пропвариант**, что позволяет использовать различные типы данных в зависимости от формата времени.</span><span class="sxs-lookup"><span data-stu-id="49216-248">The start position is given as a **PROPVARIANT**, allowing for different data types depending on the time format.</span></span> <span data-ttu-id="49216-249">Для 100-NS тип **пропвариант** является либо **VT \_ i8** , либо **VT \_ Empty**.</span><span class="sxs-lookup"><span data-stu-id="49216-249">For 100-ns, the **PROPVARIANT** type is either **VT\_I8** or **VT\_EMPTY**.</span></span> <span data-ttu-id="49216-250">Если **VT \_ i8**, **пропвариант** содержит начальную точку в 100-единицах NS.</span><span class="sxs-lookup"><span data-stu-id="49216-250">If **VT\_I8**, the **PROPVARIANT** contains the start position in 100-ns units.</span></span> <span data-ttu-id="49216-251">Значение **VT \_ Empty** имеет специальное значение "начать с текущей позиции".</span><span class="sxs-lookup"><span data-stu-id="49216-251">The value **VT\_EMPTY** has the special meaning "start at the current position."</span></span>

<span data-ttu-id="49216-252">Реализуйте метод [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49216-252">Implement the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method as follows:</span></span>

1.  <span data-ttu-id="49216-253">Проверить параметры и состояние:</span><span class="sxs-lookup"><span data-stu-id="49216-253">Validate parameters and state:</span></span>
    -   <span data-ttu-id="49216-254">Проверьте наличие параметров **null** .</span><span class="sxs-lookup"><span data-stu-id="49216-254">Check for **NULL** parameters.</span></span>
    -   <span data-ttu-id="49216-255">Проверьте GUID формата времени.</span><span class="sxs-lookup"><span data-stu-id="49216-255">Check the time-format GUID.</span></span> <span data-ttu-id="49216-256">Если значение недопустимо, возвращается **\_ \_ неподдерживаемый \_ \_ Формат времени в MF E**.</span><span class="sxs-lookup"><span data-stu-id="49216-256">If the value is invalid, return **MF\_E\_UNSUPPORTED\_TIME\_FORMAT**.</span></span>
    -   <span data-ttu-id="49216-257">Проверьте тип данных **пропвариант** , в котором находится начальная координата.</span><span class="sxs-lookup"><span data-stu-id="49216-257">Check the data type of the **PROPVARIANT** that holds the start position.</span></span>
    -   <span data-ttu-id="49216-258">Проверьте начальную точку.</span><span class="sxs-lookup"><span data-stu-id="49216-258">Validate the start position.</span></span> <span data-ttu-id="49216-259">Если значение недопустимо, возвращается **MF \_ E \_ инвалидрекуест**.</span><span class="sxs-lookup"><span data-stu-id="49216-259">If invalid, return **MF\_E\_INVALIDREQUEST**.</span></span>
    -   <span data-ttu-id="49216-260">Если работа источника была завершена, возвращайте ключ **\_ \_ завершения работы MF E**.</span><span class="sxs-lookup"><span data-stu-id="49216-260">If the source has been shut down, return **MF\_E\_SHUTDOWN**.</span></span>
2.  <span data-ttu-id="49216-261">Если на шаге 1 не возникает ошибки, поочередно помещает асинхронную операцию в очередь.</span><span class="sxs-lookup"><span data-stu-id="49216-261">If no error occurs in step 1, queue an asynchronous operation.</span></span> <span data-ttu-id="49216-262">Все после этого шага происходит в потоке рабочей очереди.</span><span class="sxs-lookup"><span data-stu-id="49216-262">Everything after this step occurs on a work-queue thread.</span></span>
3.  <span data-ttu-id="49216-263">Для каждого потока:</span><span class="sxs-lookup"><span data-stu-id="49216-263">For each stream:</span></span>
    1.  <span data-ttu-id="49216-264">Убедитесь, что поток уже активен из предыдущего запроса на [**Запуск**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) .</span><span class="sxs-lookup"><span data-stu-id="49216-264">Check if the stream is already active from a previous [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) request.</span></span>
    2.  <span data-ttu-id="49216-265">Вызовите [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) , чтобы проверить, выбрано ли приложение или отменяет выбор потока.</span><span class="sxs-lookup"><span data-stu-id="49216-265">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to check whether the application selected or deselected the stream.</span></span>
    3.  <span data-ttu-id="49216-266">Если выбранный ранее поток теперь не выбран, очистите все недоставленные образцы для этого потока.</span><span class="sxs-lookup"><span data-stu-id="49216-266">If a previously selected stream is now deselected, flush any undelivered samples for that stream.</span></span>
    4.  <span data-ttu-id="49216-267">Если поток активен, источник мультимедиа (не поток) отправляет одно из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="49216-267">If the stream is active, the media source (not the stream) sends one of the following events:</span></span>
        -   <span data-ttu-id="49216-268">Он отправляет [меупдатедстреам](meupdatedstream.md) , если поток был ранее активен.</span><span class="sxs-lookup"><span data-stu-id="49216-268">It sends [MEUpdatedStream](meupdatedstream.md) if the stream was previously active.</span></span>
        -   <span data-ttu-id="49216-269">В противном случае он отправляет [меневстреам](menewstream.md).</span><span class="sxs-lookup"><span data-stu-id="49216-269">Otherwise, it sends [MENewStream](menewstream.md).</span></span>

        <span data-ttu-id="49216-270">Для обоих событий данные события являются [**имфмедиастреам**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) указателем для потока.</span><span class="sxs-lookup"><span data-stu-id="49216-270">For both events, the event data is the [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) pointer for the stream.</span></span>
    5.  <span data-ttu-id="49216-271">Если источник перезапускается из приостановленного состояния, возможны незавершенные запросы на выборку.</span><span class="sxs-lookup"><span data-stu-id="49216-271">If the source is restarting from the paused state, there might be pending sample requests.</span></span> <span data-ttu-id="49216-272">Если да, доставьте их сейчас.</span><span class="sxs-lookup"><span data-stu-id="49216-272">If so, deliver these now.</span></span>
    6.  <span data-ttu-id="49216-273">Если источник ищет новую точку, каждый объект потока отправляет событие [местреамсикед](mestreamseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-273">If the source is seeking to a new position, each stream object sends an [MEStreamSeeked](mestreamseeked.md) event.</span></span> <span data-ttu-id="49216-274">В противном случае каждый поток отправляет событие [местреамстартед](mestreamstarted.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-274">Otherwise, each stream sends an [MEStreamStarted](mestreamstarted.md) event.</span></span>
4.  <span data-ttu-id="49216-275">Если источник ищет новую точку, источник мультимедиа отправляет событие [месаурцесикед](mesourceseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-275">If the source is seeking to a new position, the media source sends an [MESourceSeeked](mesourceseeked.md) event.</span></span> <span data-ttu-id="49216-276">В противном случае он отправляет событие [месаурцестартед](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-276">Otherwise, it sends an [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="49216-277">Если ошибка возникает в любой момент после шага 2, источник отправляет событие [месаурцестартед](mesourcestarted.md) с кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="49216-277">If an error occurs at any time after step 2, the source sends an [MESourceStarted](mesourcestarted.md) event with an error code.</span></span> <span data-ttu-id="49216-278">Это предупреждает приложение о том, что метод [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) завершился сбоем асинхронно.</span><span class="sxs-lookup"><span data-stu-id="49216-278">This alerts the application that the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method failed asynchronously.</span></span>

<span data-ttu-id="49216-279">В следующем коде показаны шаги 1 – 2.</span><span class="sxs-lookup"><span data-stu-id="49216-279">The following code shows steps 1–2:</span></span>


```C++
HRESULT MPEG1Source::Start(
        IMFPresentationDescriptor* pPresentationDescriptor,
        const GUID* pguidTimeFormat,
        const PROPVARIANT* pvarStartPos
    )
{

    HRESULT hr = S_OK;
    SourceOp *pAsyncOp = NULL;

    // Check parameters.

    // Start position and presentation descriptor cannot be NULL.
    if (pvarStartPos == NULL || pPresentationDescriptor == NULL)
    {
        return E_INVALIDARG;
    }

    // Check the time format.
    if ((pguidTimeFormat != NULL) && (*pguidTimeFormat != GUID_NULL))
    {
        // Unrecognized time format GUID.
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    // Check the data type of the start position.
    if ((pvarStartPos->vt != VT_I8) && (pvarStartPos->vt != VT_EMPTY))
    {
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    EnterCriticalSection(&m_critSec);

    // Check if this is a seek request. This sample does not support seeking.

    if (pvarStartPos->vt == VT_I8)
    {
        // If the current state is STOPPED, then position 0 is valid.
        // Otherwise, the start position must be VT_EMPTY (current position).

        if ((m_state != STATE_STOPPED) || (pvarStartPos->hVal.QuadPart != 0))
        {
            hr = MF_E_INVALIDREQUEST;
            goto done;
        }
    }

    // Fail if the source is shut down.
    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Fail if the source was not initialized yet.
    hr = IsInitialized();
    if (FAILED(hr))
    {
        goto done;
    }

    // Perform a basic check on the caller's presentation descriptor.
    hr = ValidatePresentationDescriptor(pPresentationDescriptor);
    if (FAILED(hr))
    {
        goto done;
    }

    // The operation looks OK. Complete the operation asynchronously.
    hr = SourceOp::CreateStartOp(pPresentationDescriptor, &pAsyncOp);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAsyncOp->SetData(*pvarStartPos);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = QueueOperation(pAsyncOp);

done:
    SafeRelease(&pAsyncOp);
    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



<span data-ttu-id="49216-280">Остальные шаги показаны в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="49216-280">The remaining steps are shown in the next example:</span></span>


```C++
HRESULT MPEG1Source::DoStart(StartOp *pOp)
{
    assert(pOp->Op() == SourceOp::OP_START);

    IMFPresentationDescriptor *pPD = NULL;
    IMFMediaEvent  *pEvent = NULL;

    HRESULT     hr = S_OK;
    LONGLONG    llStartOffset = 0;
    BOOL        bRestartFromCurrentPosition = FALSE;
    BOOL        bSentEvents = FALSE;

    hr = BeginAsyncOp(pOp);

    // Get the presentation descriptor from the SourceOp object.
    // This is the PD that the caller passed into the Start() method.
    // The PD has already been validated.
    if (SUCCEEDED(hr))
    {
        hr = pOp->GetPresentationDescriptor(&pPD);
    }

    // Because this sample does not support seeking, the start
    // position must be 0 (from stopped) or "current position."

    // If the sample supported seeking, we would need to get the
    // start position from the PROPVARIANT data contained in pOp.

    if (SUCCEEDED(hr))
    {
        // Select/deselect streams, based on what the caller set in the PD.
        // This method also sends the MENewStream/MEUpdatedStream events.
        hr = SelectStreams(pPD, pOp->Data());
    }

    if (SUCCEEDED(hr))
    {
        m_state = STATE_STARTED;

        // Queue the "started" event. The event data is the start position.
        hr = m_pEventQueue->QueueEventParamVar(
            MESourceStarted,
            GUID_NULL,
            S_OK,
            &pOp->Data()
            );
    }

    if (FAILED(hr))
    {
        // Failure. Send the error code to the application.

        // Note: It's possible that QueueEvent itself failed, in which case it
        // is likely to fail again. But there is no good way to recover in
        // that case.

        (void)m_pEventQueue->QueueEventParamVar(
            MESourceStarted, GUID_NULL, hr, NULL);
    }

    CompleteAsyncOp(pOp);

    SafeRelease(&pEvent);
    SafeRelease(&pPD);
    return hr;
}
```



### <a name="pause"></a><span data-ttu-id="49216-281">Пауза</span><span class="sxs-lookup"><span data-stu-id="49216-281">Pause</span></span>

<span data-ttu-id="49216-282">Метод [**имфмедиасаурце::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) приостанавливает источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-282">The [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method pauses the media source.</span></span> <span data-ttu-id="49216-283">Реализуйте этот метод следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49216-283">Implement this method as follows:</span></span>

1.  <span data-ttu-id="49216-284">Постановка асинхронной операции в очередь.</span><span class="sxs-lookup"><span data-stu-id="49216-284">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="49216-285">Каждый активный поток отправляет событие [местреампаусед](mestreampaused.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-285">Each active stream sends an [MEStreamPaused](mestreampaused.md) event.</span></span>
3.  <span data-ttu-id="49216-286">Источник мультимедиа отправляет событие [месаурцепаусед](mesourcepaused.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-286">The media source sends an [MESourcePaused](mesourcepaused.md) event.</span></span>

<span data-ttu-id="49216-287">При приостановке, исходная очередь помещает запросы на выборку, не обрабатывая их.</span><span class="sxs-lookup"><span data-stu-id="49216-287">While paused, the source queues sample requests without processing them.</span></span> <span data-ttu-id="49216-288">(См. [примеры запросов](#sample-requests).)</span><span class="sxs-lookup"><span data-stu-id="49216-288">(See [Sample Requests](#sample-requests).)</span></span>

### <a name="stop"></a><span data-ttu-id="49216-289">Stop</span><span class="sxs-lookup"><span data-stu-id="49216-289">Stop</span></span>

<span data-ttu-id="49216-290">Метод [**имфмедиасаурце:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) останавливает источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-290">The [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method stops the media source.</span></span> <span data-ttu-id="49216-291">Реализуйте этот метод следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49216-291">Implement this method as follows:</span></span>

1.  <span data-ttu-id="49216-292">Постановка асинхронной операции в очередь.</span><span class="sxs-lookup"><span data-stu-id="49216-292">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="49216-293">Каждый активный поток отправляет событие [местреамстоппед](mestreamstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-293">Each active stream sends an [MEStreamStopped](mestreamstopped.md) event.</span></span>
3.  <span data-ttu-id="49216-294">Очистите все образцы в очереди и примеры запросов.</span><span class="sxs-lookup"><span data-stu-id="49216-294">Clear all queued samples and sample requests.</span></span>
4.  <span data-ttu-id="49216-295">Источник мультимедиа отправляет событие [месаурцестоппед](mesourcestopped.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-295">The media source sends an [MESourceStopped](mesourcestopped.md) event.</span></span>

<span data-ttu-id="49216-296">При остановке источник отклоняет все запросы к примерам.</span><span class="sxs-lookup"><span data-stu-id="49216-296">While stopped, the source rejects all requests for samples.</span></span>

<span data-ttu-id="49216-297">Если источник остановлен во время выполнения запроса ввода-вывода, запрос ввода-вывода может завершиться после того, как источник войдет в остановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="49216-297">If the source is stopped while an I/O request is in progress, the I/O request might complete after the source enters the stopped state.</span></span> <span data-ttu-id="49216-298">В этом случае источник должен отменить результат этого запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="49216-298">In that case, the source should discard the result of that I/O request.</span></span>

## <a name="sample-requests"></a><span data-ttu-id="49216-299">Образец запросов</span><span class="sxs-lookup"><span data-stu-id="49216-299">Sample Requests</span></span>

<span data-ttu-id="49216-300">Media Foundation использовать модель *извлечения* , в которой конвейер запрашивает образцы из источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-300">Media Foundation use a *pull* model, in which the pipeline requests samples from the media source.</span></span> <span data-ttu-id="49216-301">Это отличается от модели, используемой DirectShow, в которой образцы источников push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="49216-301">This differs from the model used by DirectShow, in which the sources "pushes" samples.</span></span>

<span data-ttu-id="49216-302">Чтобы запросить новый пример, Media Foundation конвейер вызывает метод [**имфмедиастреам:: рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span><span class="sxs-lookup"><span data-stu-id="49216-302">To request a new sample, the Media Foundation pipeline calls [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span> <span data-ttu-id="49216-303">Этот метод принимает указатель **IUnknown** , представляющий объект *маркера* .</span><span class="sxs-lookup"><span data-stu-id="49216-303">This method takes an **IUnknown** pointer that represents a *token* object.</span></span> <span data-ttu-id="49216-304">Реализация объекта токена находится в вызывающем объекте; Он просто предоставляет вызывающему объекту способ для трассировки запросов выборки.</span><span class="sxs-lookup"><span data-stu-id="49216-304">The implementation of the token object is up to the caller; it simply provides a way for the caller to track sample requests.</span></span> <span data-ttu-id="49216-305">Параметр token может также иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="49216-305">The token parameter can also be **NULL**.</span></span>

<span data-ttu-id="49216-306">Предполагая, что источник использует асинхронные запросы ввода-вывода для чтения данных, создание примеров не будет синхронизировано с примерами запросов.</span><span class="sxs-lookup"><span data-stu-id="49216-306">Assuming the source uses asynchronous I/O requests to read data, sample generation will not be synchronized with sample requests.</span></span> <span data-ttu-id="49216-307">Чтобы синхронизировать примеры запросов с примером создания, источник мультимедиа выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="49216-307">To synchronize sample requests with sample generation, a media source does the following:</span></span>

1.  <span data-ttu-id="49216-308">Маркеры запроса помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="49216-308">Request tokens are placed on a queue.</span></span>
2.  <span data-ttu-id="49216-309">При создании образцов они помещаются во вторую очередь.</span><span class="sxs-lookup"><span data-stu-id="49216-309">As samples are generated, they are placed on a second queue.</span></span>
3.  <span data-ttu-id="49216-310">Источник мультимедиа завершает пример запроса, получая маркер запроса из первой очереди и пример из второй очереди.</span><span class="sxs-lookup"><span data-stu-id="49216-310">The media source completes a sample request by pulling a request token from the first queue and a sample from the second queue.</span></span>
4.  <span data-ttu-id="49216-311">Источник мультимедиа отправляет событие Мемедиасампле.</span><span class="sxs-lookup"><span data-stu-id="49216-311">The media source sends an MEMediaSample event.</span></span> <span data-ttu-id="49216-312">Событие содержит указатель на образец, а образец содержит указатель на маркер.</span><span class="sxs-lookup"><span data-stu-id="49216-312">The event contains a pointer to the sample, and the sample contains a pointer to the token.</span></span>

<span data-ttu-id="49216-313">На следующей схеме показана связь между событием [мемедиасампле](memediasample.md) , образцом и маркером запроса.</span><span class="sxs-lookup"><span data-stu-id="49216-313">The following diagram shows the relationship between the [MEMediaSample](memediasample.md) event, the sample, and the request token.</span></span>

![Диаграмма, показывающая мемедиасампле, и пример очереди, указывающий на имфсампле; имфсампле и очередь запросов указывают на IUnknown](images/mediasourceimpl01.png)

<span data-ttu-id="49216-315">В примере источника MPEG-1 этот процесс реализуется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49216-315">The example MPEG-1 source implements this process as follows:</span></span>

1.  <span data-ttu-id="49216-316">Метод [**рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) помещает запрос в очередь FIFO.</span><span class="sxs-lookup"><span data-stu-id="49216-316">The [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method puts the request on a FIFO queue.</span></span>
2.  <span data-ttu-id="49216-317">По мере завершения запросов ввода-вывода источник мультимедиа создает новые образцы и помещает их во вторую очередь FIFO.</span><span class="sxs-lookup"><span data-stu-id="49216-317">As I/O requests are completed, the media source creates new samples and puts them on a second FIFO queue.</span></span> <span data-ttu-id="49216-318">(Эта очередь имеет максимальный размер, чтобы предотвратить слишком далекое чтение источника.)</span><span class="sxs-lookup"><span data-stu-id="49216-318">(This queue has a maximum size, to prevent the source from reading too far ahead.)</span></span>
3.  <span data-ttu-id="49216-319">Если обе эти очереди имеют по крайней мере один элемент (один запрос и один пример), источник мультимедиа завершает первый запрос из очереди запросов, отправляя первый пример из очереди.</span><span class="sxs-lookup"><span data-stu-id="49216-319">Whenever both of these queues have at least one item (one request and one sample), the media source completes the first request from the request queue by sending out the first sample from the sample queue.</span></span>
4.  <span data-ttu-id="49216-320">Для доставки примера объект потока (не исходный объект) отправляет событие [мемедиасампле](memediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-320">To deliver a sample, the stream object (not the source object) sends an [MEMediaSample](memediasample.md) event.</span></span>
    -   <span data-ttu-id="49216-321">Данные события являются указателем на интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) образца.</span><span class="sxs-lookup"><span data-stu-id="49216-321">The event data is a pointer to the sample's [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span>
    -   <span data-ttu-id="49216-322">Если запрос включал маркер, присоедините маркер к образцу, установив атрибут [**\_ токена мфсампликстенсион**](mfsampleextension-token-attribute.md) в образце.</span><span class="sxs-lookup"><span data-stu-id="49216-322">If the request included a token, attach the token to the sample by setting the [**MFSampleExtension\_Token**](mfsampleextension-token-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="49216-323">На этом этапе есть три возможности:</span><span class="sxs-lookup"><span data-stu-id="49216-323">At this point, there are three possibilities:</span></span>

-   <span data-ttu-id="49216-324">Существует еще один пример в очереди образцов, но нет соответствующего запроса.</span><span class="sxs-lookup"><span data-stu-id="49216-324">There is another sample in the sample queue, but no matching request.</span></span>
-   <span data-ttu-id="49216-325">Существует запрос, но нет примера.</span><span class="sxs-lookup"><span data-stu-id="49216-325">There is a request, but no sample.</span></span>
-   <span data-ttu-id="49216-326">Обе очереди пусты; нет примеров и запросов.</span><span class="sxs-lookup"><span data-stu-id="49216-326">Both queues are empty; there are no samples and no requests.</span></span>

<span data-ttu-id="49216-327">Если пример очереди пуст, источник проверяет конец потока (см. [конец потока](#end-of-stream)).</span><span class="sxs-lookup"><span data-stu-id="49216-327">If the sample queue is empty, the source checks for the end of the stream (see [End of Stream](#end-of-stream)).</span></span> <span data-ttu-id="49216-328">В противном случае он запускает другой запрос ввода-вывода для данных.</span><span class="sxs-lookup"><span data-stu-id="49216-328">Otherwise, it starts another I/O request for data.</span></span> <span data-ttu-id="49216-329">Если во время этого процесса возникает какая либо ошибка, поток отправляет событие [Миррор](meerror.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-329">If any error occurs during this process, the stream sends an [MEError](meerror.md) event.</span></span>

<span data-ttu-id="49216-330">В следующем коде реализуется метод [**имфмедиастреам:: рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) :</span><span class="sxs-lookup"><span data-stu-id="49216-330">The following code implements the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method:</span></span>


```C++
HRESULT MPEG1Stream::RequestSample(IUnknown* pToken)
{
    HRESULT hr = S_OK;
    IMFMediaSource *pSource = NULL;

    // Hold the media source object's critical section.
    SourceLock lock(m_pSource);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_state == STATE_STOPPED)
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (!m_bActive)
    {
        // If the stream is not active, it should not get sample requests.
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (m_bEOS && m_Samples.IsEmpty())
    {
        // This stream has already reached the end of the stream, and the
        // sample queue is empty.
        hr = MF_E_END_OF_STREAM;
        goto done;
    }

    hr = m_Requests.InsertBack(pToken);
    if (FAILED(hr))
    {
        goto done;
    }

    // Dispatch the request.
    hr = DispatchSamples();
    if (FAILED(hr))
    {
        goto done;
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        hr = m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }
    return hr;
}
```



<span data-ttu-id="49216-331">`DispatchSamples`Метод извлекает образцы из очереди образцов, сопоставляет их с ожидающими запросами выборки и помещает в очередь события [мемедиасампле](memediasample.md) :</span><span class="sxs-lookup"><span data-stu-id="49216-331">The `DispatchSamples` method pulls samples from the sample queue, matches them with pending sample requests, and queues [MEMediaSample](memediasample.md) events:</span></span>


```C++
HRESULT MPEG1Stream::DispatchSamples()
{
    HRESULT hr = S_OK;
    BOOL bNeedData = FALSE;
    BOOL bEOS = FALSE;

    SourceLock lock(m_pSource);

    // An I/O request can complete after the source is paused, stopped, or
    // shut down. Do not deliver samples unless the source is running.
    if (m_state != STATE_STARTED)
    {
        return S_OK;
    }

    IMFSample *pSample = NULL;
    IUnknown  *pToken = NULL;

    // Deliver as many samples as we can.
    while (!m_Samples.IsEmpty() && !m_Requests.IsEmpty())
    {
        // Pull the next sample from the queue.
        hr = m_Samples.RemoveFront(&pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Pull the next request token from the queue. Tokens can be NULL.
        hr = m_Requests.RemoveFront(&pToken);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pToken)
        {
            // Set the token on the sample.
            hr = pSample->SetUnknown(MFSampleExtension_Token, pToken);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Send an MEMediaSample event with the sample.
        hr = m_pEventQueue->QueueEventParamUnk(
            MEMediaSample, GUID_NULL, S_OK, pSample);

        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pSample);
        SafeRelease(&pToken);
    }

    if (m_Samples.IsEmpty() && m_bEOS)
    {
        // The sample queue is empty AND we have reached the end of the source
        // stream. Notify the pipeline by sending the end-of-stream event.

        hr = m_pEventQueue->QueueEventParamVar(
            MEEndOfStream, GUID_NULL, S_OK, NULL);

        if (FAILED(hr))
        {
            goto done;
        }

        // Notify the source. It will send the end-of-presentation event.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_END_OF_STREAM);
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (NeedsData())
    {
        // The sample queue is empty; the request queue is not empty; and we
        // have not reached the end of the stream. Ask for more data.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_REQUEST_DATA);
        if (FAILED(hr))
        {
            goto done;
        }
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }

    SafeRelease(&pSample);
    SafeRelease(&pToken);
    return S_OK;
}
```



<span data-ttu-id="49216-332">`DispatchSamples`Метод вызывается в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="49216-332">The `DispatchSamples` method is called in the following circumstances:</span></span>

-   <span data-ttu-id="49216-333">Внутри метода [**рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="49216-333">Inside the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>
-   <span data-ttu-id="49216-334">При перезапуске источника мультимедиа из приостановленного состояния.</span><span class="sxs-lookup"><span data-stu-id="49216-334">When the media source restarts from the paused state.</span></span>
-   <span data-ttu-id="49216-335">При завершении запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="49216-335">When an I/O request completes.</span></span>

## <a name="end-of-stream"></a><span data-ttu-id="49216-336">Конец потока</span><span class="sxs-lookup"><span data-stu-id="49216-336">End of Stream</span></span>

<span data-ttu-id="49216-337">Если поток больше не содержит данных и все образцы для этого потока были доставлены, объекты потока отправляют событие [миндофстреам](meendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-337">When a stream has no more data, and all of the samples for that stream have been delivered, the stream objects sends an [MEEndOfStream](meendofstream.md) event.</span></span>

<span data-ttu-id="49216-338">Когда все активные потоки будут выполнены, источник мультимедиа отправляет событие [миндофпресентатион](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="49216-338">When all of the active streams are done, the media source sends an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

## <a name="asynchronous-operations"></a><span data-ttu-id="49216-339">Асинхронные операции</span><span class="sxs-lookup"><span data-stu-id="49216-339">Asynchronous Operations</span></span>

<span data-ttu-id="49216-340">Возможно, самая сложная часть написания источника мультимедиа — понимание Media Foundation асинхронной модели.</span><span class="sxs-lookup"><span data-stu-id="49216-340">Perhaps the hardest part of writing a media source is understanding the Media Foundation asynchronous model.</span></span>

<span data-ttu-id="49216-341">Все методы в источнике мультимедиа, которые управляют потоковой передачей, являются асинхронными.</span><span class="sxs-lookup"><span data-stu-id="49216-341">All of the methods on a media source that control streaming are asynchronous.</span></span> <span data-ttu-id="49216-342">В каждом случае метод выполняет некоторую начальную проверку, например проверку параметров.</span><span class="sxs-lookup"><span data-stu-id="49216-342">In each case, the method does some initial validation, such as checking parameters.</span></span> <span data-ttu-id="49216-343">Затем источник отправляет оставшуюся часть работы в рабочую очередь.</span><span class="sxs-lookup"><span data-stu-id="49216-343">The source then dispatches the rest of the work to a work queue.</span></span> <span data-ttu-id="49216-344">По завершении операции источник мультимедиа отправляет событие обратно вызывающему объекту через интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-344">After the operation completes, the media source sends an event back to the caller, through the media source's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="49216-345">Поэтому важно понимать рабочие очереди.</span><span class="sxs-lookup"><span data-stu-id="49216-345">It is therefore important to understand work queues.</span></span>

<span data-ttu-id="49216-346">Чтобы поместить элемент в рабочую очередь, можно вызвать либо [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) , либо [**мфпутворкитемекс**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span><span class="sxs-lookup"><span data-stu-id="49216-346">To put an item on a work queue, you can call either [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) or [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span></span> <span data-ttu-id="49216-347">Источник MPEG-1 использует **мфпутворкитем**, но две функции выполняют одно и то же действие.</span><span class="sxs-lookup"><span data-stu-id="49216-347">The MPEG-1 source happens to use **MFPutWorkItem**, but the two functions do the same thing.</span></span> <span data-ttu-id="49216-348">Функция **мфпутворкитем** принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="49216-348">The **MFPutWorkItem** function takes the following parameters:</span></span>

-   <span data-ttu-id="49216-349">Значение **типа DWORD** , идентифицирующее рабочую очередь.</span><span class="sxs-lookup"><span data-stu-id="49216-349">A **DWORD** value that identifies the work queue.</span></span> <span data-ttu-id="49216-350">Вы можете создать частную рабочую очередь или использовать **\_ \_ \_ стандартную очередь обратного вызова мфасинк**.</span><span class="sxs-lookup"><span data-stu-id="49216-350">You can create a private work queue or use **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**.</span></span>
-   <span data-ttu-id="49216-351">Указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="49216-351">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="49216-352">Этот интерфейс обратного вызова вызывается для выполнения работы.</span><span class="sxs-lookup"><span data-stu-id="49216-352">This callback interface is invoked to perform the work.</span></span>
-   <span data-ttu-id="49216-353">Необязательный объект состояния, который должен реализовывать **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="49216-353">An optional state object, which must implement **IUnknown**.</span></span>

<span data-ttu-id="49216-354">Рабочая очередь обслуживается одним или несколькими рабочими потоками, которые постоянно извлекают следующий рабочий элемент из очереди и вызывают метод [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) интерфейса обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="49216-354">The work queue is serviced by one or more worker threads that continuously pull the next work item from the queue and invoke the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the callback interface.</span></span>

<span data-ttu-id="49216-355">Рабочие элементы не гарантированно выполняются в том же порядке, в котором они были помещены в очередь.</span><span class="sxs-lookup"><span data-stu-id="49216-355">Work items are not guaranteed to execute in the same order that you put them on the queue.</span></span> <span data-ttu-id="49216-356">Помните, что несколько потоков могут обслуживать одну и ту же рабочую очередь, поэтому вызовы [**вызова**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) могут перекрываться или происходить в неопределенном порядке.</span><span class="sxs-lookup"><span data-stu-id="49216-356">Remember that more than one thread can service the same work queue, so [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) calls can overlap or occur out of order.</span></span> <span data-ttu-id="49216-357">Таким образом, источник мультимедиа должен поддерживать правильное внутреннее состояние путем отправки элементов рабочей очереди в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="49216-357">Therefore, it is up to the media source to maintain the correct internal state, by submitting work queue items in the right order.</span></span> <span data-ttu-id="49216-358">При выполнении предыдущей операции источник начинает следующую операцию.</span><span class="sxs-lookup"><span data-stu-id="49216-358">Only when the previous operation is complete does the source start the next operation.</span></span>

<span data-ttu-id="49216-359">Для представления ожидающих операций источник MPEG-1 определяет класс с именем `SourceOp` :</span><span class="sxs-lookup"><span data-stu-id="49216-359">To represent pending operations, the MPEG-1 source defines a class named `SourceOp`:</span></span>


```C++
// Represents a request for an asynchronous operation.

class SourceOp : public IUnknown
{
public:

    enum Operation
    {
        OP_START,
        OP_PAUSE,
        OP_STOP,
        OP_REQUEST_DATA,
        OP_END_OF_STREAM
    };

    static HRESULT CreateOp(Operation op, SourceOp **ppOp);
    static HRESULT CreateStartOp(IMFPresentationDescriptor *pPD, SourceOp **ppOp);

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    SourceOp(Operation op);
    virtual ~SourceOp();

    HRESULT SetData(const PROPVARIANT& var);

    Operation Op() const { return m_op; }
    const PROPVARIANT& Data() { return m_data;}

protected:
    long        m_cRef;     // Reference count.
    Operation   m_op;
    PROPVARIANT m_data;     // Data for the operation.
};
```



<span data-ttu-id="49216-360">`Operation`Перечисление определяет, какая операция находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="49216-360">The `Operation` enumeration identifies which operation is pending.</span></span> <span data-ttu-id="49216-361">Класс также содержит **пропвариант** для передачи дополнительных данных для операции.</span><span class="sxs-lookup"><span data-stu-id="49216-361">The class also contains a **PROPVARIANT** to convey any additional data for the operation.</span></span>

### <a name="operation-queue"></a><span data-ttu-id="49216-362">Очередь операций</span><span class="sxs-lookup"><span data-stu-id="49216-362">Operation Queue</span></span>

<span data-ttu-id="49216-363">Для сериализации операций источник мультимедиа поддерживает очередь `SourceOp` объектов.</span><span class="sxs-lookup"><span data-stu-id="49216-363">To serialize operations, the media source maintains a queue of `SourceOp` objects.</span></span> <span data-ttu-id="49216-364">Для управления очередью используется вспомогательный класс:</span><span class="sxs-lookup"><span data-stu-id="49216-364">It uses a helper class to manage the queue:</span></span>


```C++
template <class OP_TYPE>
class OpQueue : public IUnknown
{
public:

    typedef ComPtrList<OP_TYPE>   OpList;

    HRESULT QueueOperation(OP_TYPE *pOp);

protected:

    HRESULT ProcessQueue();
    HRESULT ProcessQueueAsync(IMFAsyncResult *pResult);

    virtual HRESULT DispatchOperation(OP_TYPE *pOp) = 0;
    virtual HRESULT ValidateOperation(OP_TYPE *pOp) = 0;

    OpQueue(CRITICAL_SECTION& critsec)
        : m_OnProcessQueue(this, &OpQueue::ProcessQueueAsync),
          m_critsec(critsec)
    {
    }

    virtual ~OpQueue()
    {
    }

protected:
    OpList                  m_OpQueue;         // Queue of operations.
    CRITICAL_SECTION&       m_critsec;         // Protects the queue state.
    AsyncCallback<OpQueue>  m_OnProcessQueue;  // ProcessQueueAsync callback.
};
```



<span data-ttu-id="49216-365">`OpQueue`Класс предназначен для наследования компонентом, выполняющим асинхронные рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="49216-365">The `OpQueue` class is designed to be inherited by the component that performs asynchronous work items.</span></span> <span data-ttu-id="49216-366">Параметр *шаблона \_ типа Op* — это тип объекта, используемый для представления рабочих элементов в очереди. в данном случае *\_ типом Op* будет `SourceOp` .</span><span class="sxs-lookup"><span data-stu-id="49216-366">The *OP\_TYPE* template parameter is the object type used to represent work items in the queue—in this case, *OP\_TYPE* will be `SourceOp`.</span></span> <span data-ttu-id="49216-367">`OpQueue`Класс реализует следующие методы:</span><span class="sxs-lookup"><span data-stu-id="49216-367">The `OpQueue` class implements the following methods:</span></span>

-   <span data-ttu-id="49216-368">`QueueOperation` помещает новый элемент в очередь.</span><span class="sxs-lookup"><span data-stu-id="49216-368">`QueueOperation` puts a new item on the queue.</span></span>
-   <span data-ttu-id="49216-369">`ProcessQueue` отправляет следующую операцию из очереди.</span><span class="sxs-lookup"><span data-stu-id="49216-369">`ProcessQueue` dispatches the next operation from the queue.</span></span> <span data-ttu-id="49216-370">Этот метод является асинхронным.</span><span class="sxs-lookup"><span data-stu-id="49216-370">This method is asynchronous.</span></span>
-   <span data-ttu-id="49216-371">`ProcessQueueAsync` Завершает асинхронный `ProcessQueue` метод.</span><span class="sxs-lookup"><span data-stu-id="49216-371">`ProcessQueueAsync` completes the asynchronous `ProcessQueue` method.</span></span>

<span data-ttu-id="49216-372">Производным классом должен быть реализован еще два метода:</span><span class="sxs-lookup"><span data-stu-id="49216-372">Another two methods must be implemented by the derived class:</span></span>

-   <span data-ttu-id="49216-373">`ValidateOperation` проверяет, является ли он допустимым для выполнения указанной операции с учетом текущего состояния источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-373">`ValidateOperation` checks whether it is valid to perform a specified operation, given the current state of the media source.</span></span>
-   <span data-ttu-id="49216-374">`DispatchOperation` выполняет асинхронный рабочий элемент.</span><span class="sxs-lookup"><span data-stu-id="49216-374">`DispatchOperation` carries out the asynchronous work item.</span></span>

<span data-ttu-id="49216-375">Очередь операций используется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49216-375">The operation queue is used as follows:</span></span>

1.  <span data-ttu-id="49216-376">Конвейер Media Foundation вызывает асинхронный метод в источнике мультимедиа, например [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="49216-376">The Media Foundation pipeline calls an asynchronous method on the media source, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="49216-377">Асинхронный метод вызывает `QueueOperation` , который помещает [**начальную**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) операцию в очередь и вызывает `ProcessQueue` (в форме `SourceOp` объекта).</span><span class="sxs-lookup"><span data-stu-id="49216-377">The asynchronous method calls `QueueOperation`, which puts the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) operation on the queue and calls `ProcessQueue` (in the form of a `SourceOp` object).</span></span>
3.  <span data-ttu-id="49216-378">`ProcessQueue` вызывает [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span><span class="sxs-lookup"><span data-stu-id="49216-378">`ProcessQueue` calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span>
4.  <span data-ttu-id="49216-379">Поток рабочей очереди вызывает `ProcessQueueAsync` .</span><span class="sxs-lookup"><span data-stu-id="49216-379">The work-queue thread calls `ProcessQueueAsync`.</span></span>
5.  <span data-ttu-id="49216-380">`ProcessQueueAsync`Метод вызывает `ValidateOperation` и `DispatchOperation` .</span><span class="sxs-lookup"><span data-stu-id="49216-380">The `ProcessQueueAsync` method calls `ValidateOperation` and `DispatchOperation`.</span></span>

<span data-ttu-id="49216-381">Следующий код помещает новую операцию в источник MPEG-1:</span><span class="sxs-lookup"><span data-stu-id="49216-381">The following code queues a new operation on the MPEG-1 source:</span></span>


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::QueueOperation(OP_TYPE *pOp)
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_critsec);

    hr = m_OpQueue.InsertBack(pOp);
    if (SUCCEEDED(hr))
    {
        hr = ProcessQueue();
    }

    LeaveCriticalSection(&m_critsec);
    return hr;
}
```



<span data-ttu-id="49216-382">Следующий код обрабатывает очередь:</span><span class="sxs-lookup"><span data-stu-id="49216-382">The following code processes the queue:</span></span>


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::ProcessQueue()
{
    HRESULT hr = S_OK;
    if (m_OpQueue.GetCount() > 0)
    {
        hr = MFPutWorkItem(
            MFASYNC_CALLBACK_QUEUE_STANDARD,    // Use the standard work queue.
            &m_OnProcessQueue,                  // Callback method.
            NULL                                // State object.
            );
    }
    return hr;
}
```



<span data-ttu-id="49216-383">`ValidateOperation`Метод проверяет, может ли источник MPEG-1 отправлять следующую операцию в очереди.</span><span class="sxs-lookup"><span data-stu-id="49216-383">The `ValidateOperation` method checks whether the MPEG-1 source can dispatch the next operation in the queue.</span></span> <span data-ttu-id="49216-384">Если выполняется другая операция, `ValidateOperation` возвращает **MF \_ E \_ нотакцептинг**.</span><span class="sxs-lookup"><span data-stu-id="49216-384">If another operation is in progress, `ValidateOperation` returns **MF\_E\_NOTACCEPTING**.</span></span> <span data-ttu-id="49216-385">Это гарантирует, что `DispatchOperation` при наличии другой ожидающей операции она не вызывается.</span><span class="sxs-lookup"><span data-stu-id="49216-385">This ensures that `DispatchOperation` is not called while there is another operation pending.</span></span>


```C++
HRESULT MPEG1Source::ValidateOperation(SourceOp *pOp)
{
    if (m_pCurrentOp != NULL)
    {
        return MF_E_NOTACCEPTING;
    }
    return S_OK;
}
```



<span data-ttu-id="49216-386">Метод DispatchOperation переключается по типу операции:</span><span class="sxs-lookup"><span data-stu-id="49216-386">The DispatchOperation method switches on the operation type:</span></span>


```C++
//-------------------------------------------------------------------
// DispatchOperation
//
// Performs the asynchronous operation indicated by pOp.
//
// NOTE:
// This method implements the pure-virtual OpQueue::DispatchOperation
// method. It is always called from a work-queue thread.
//-------------------------------------------------------------------

HRESULT MPEG1Source::DispatchOperation(SourceOp *pOp)
{
    EnterCriticalSection(&m_critSec);

    HRESULT hr = S_OK;

    if (m_state == STATE_SHUTDOWN)
    {
        LeaveCriticalSection(&m_critSec);

        return S_OK; // Already shut down, ignore the request.
    }

    switch (pOp->Op())
    {

    // IMFMediaSource methods:

    case SourceOp::OP_START:
        hr = DoStart((StartOp*)pOp);
        break;

    case SourceOp::OP_STOP:
        hr = DoStop(pOp);
        break;

    case SourceOp::OP_PAUSE:
        hr = DoPause(pOp);
        break;

    // Operations requested by the streams:

    case SourceOp::OP_REQUEST_DATA:
        hr = OnStreamRequestSample(pOp);
        break;

    case SourceOp::OP_END_OF_STREAM:
        hr = OnEndOfStream(pOp);
        break;

    default:
        hr = E_UNEXPECTED;
    }

    if (FAILED(hr))
    {
        StreamingError(hr);
    }

    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



<span data-ttu-id="49216-387">Подведение итогов.</span><span class="sxs-lookup"><span data-stu-id="49216-387">To summarize:</span></span>

1.  <span data-ttu-id="49216-388">Конвейер вызывает асинхронный метод, например [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="49216-388">The pipeline calls an asynchronous method, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="49216-389">Асинхронный метод вызывает `OpQueue::QueueOperation` , передавая указатель на `SourceOp` объект.</span><span class="sxs-lookup"><span data-stu-id="49216-389">The asynchronous method calls `OpQueue::QueueOperation`, passing in a pointer to a `SourceOp` object.</span></span>
3.  <span data-ttu-id="49216-390">`QueueOperation`Метод помещает операцию в очередь *\_ опкуеуе m* и вызывает `OpQueue::ProcessQueue` .</span><span class="sxs-lookup"><span data-stu-id="49216-390">The `QueueOperation` method puts the operation on the *m\_OpQueue* queue and calls `OpQueue::ProcessQueue`.</span></span>
4.  <span data-ttu-id="49216-391">`ProcessQueue`Метод вызывает [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span><span class="sxs-lookup"><span data-stu-id="49216-391">The `ProcessQueue` method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span> <span data-ttu-id="49216-392">С этого момента все происходит в Media Foundation потоке рабочей очереди.</span><span class="sxs-lookup"><span data-stu-id="49216-392">From this point, everything happens on a Media Foundation work-queue thread.</span></span> <span data-ttu-id="49216-393">Асинхронный метод возвращает вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="49216-393">The asynchronous method returns to the caller.</span></span>
5.  <span data-ttu-id="49216-394">Поток рабочей очереди вызывает `OpQueue::ProcessQueueAsync` метод.</span><span class="sxs-lookup"><span data-stu-id="49216-394">The work-queue thread calls the `OpQueue::ProcessQueueAsync` method.</span></span>
6.  <span data-ttu-id="49216-395">`ProcessQueueAsync`Метод вызывает `MPEG1Source:ValidateOperation` для проверки операции.</span><span class="sxs-lookup"><span data-stu-id="49216-395">The `ProcessQueueAsync` method calls `MPEG1Source:ValidateOperation` to validate the operation.</span></span>
7.  <span data-ttu-id="49216-396">`ProcessQueueAsync`Метод вызывает `MPEG1Source::DispatchOperation` для обработки операции.</span><span class="sxs-lookup"><span data-stu-id="49216-396">The `ProcessQueueAsync` method calls `MPEG1Source::DispatchOperation` to process the operation.</span></span>

<span data-ttu-id="49216-397">Эта схема имеет несколько преимуществ.</span><span class="sxs-lookup"><span data-stu-id="49216-397">There are several benefits to this design:</span></span>

-   <span data-ttu-id="49216-398">Методы являются асинхронными, поэтому они не блокируют поток вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="49216-398">Methods are asynchronous, so they do not block the calling application's thread.</span></span>
-   <span data-ttu-id="49216-399">Операции отправляются в поток рабочих очередей Media Foundation, который совместно используется компонентами конвейера.</span><span class="sxs-lookup"><span data-stu-id="49216-399">Operations are dispatched on a Media Foundation work-queue thread, which is shared among pipeline components.</span></span> <span data-ttu-id="49216-400">Таким образом, источник мультимедиа не создает собственный поток, уменьшая общее количество создаваемых потоков.</span><span class="sxs-lookup"><span data-stu-id="49216-400">Therefore, the media source does not create its own thread, reducing the total number of threads that are created.</span></span>
-   <span data-ttu-id="49216-401">Источник мультимедиа не блокируется при ожидании завершения операций.</span><span class="sxs-lookup"><span data-stu-id="49216-401">The media source does not block while waiting for operations to complete.</span></span> <span data-ttu-id="49216-402">Это снижает вероятность того, что источник мультимедиа случайным образом вызовет взаимоблокировку и помогает сократить переключение контекста.</span><span class="sxs-lookup"><span data-stu-id="49216-402">This reduces the chance that a media source will accidentally cause a deadlock, and helps to reduce context switching.</span></span>
-   <span data-ttu-id="49216-403">Источник мультимедиа может использовать асинхронный ввод-вывод для чтения исходного файла (путем вызова [**имфбитестреам:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span><span class="sxs-lookup"><span data-stu-id="49216-403">The media source can use asynchronous I/O to read the source file (by calling [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span></span> <span data-ttu-id="49216-404">Источник мультимедиа не требуется блокировать при ожидании завершения подпрограммы ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="49216-404">The media source does not need to block while waiting for I/O routine complete.</span></span>

<span data-ttu-id="49216-405">Если следовать шаблону, показанному в примере пакета SDK, вы можете сосредоточиться на конкретных деталях источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49216-405">If you follow the pattern shown in the SDK sample, you can focus on the particular details of your media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49216-406">См. также</span><span class="sxs-lookup"><span data-stu-id="49216-406">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49216-407">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="49216-407">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="49216-408">Запись пользовательского источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="49216-408">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 



