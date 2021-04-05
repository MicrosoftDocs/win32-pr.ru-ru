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
# <a name="case-study-mpeg-1-media-source"></a>Пример использования: источник мультимедиа MPEG-1

В Microsoft Media Foundation объект, который представляет данные мультимедиа в конвейере данных, называется *источником мультимедиа*. В этом разделе приведен подробный обзор примера пакета SDK [MPEG-1 Media Source](mpeg1source-sample.md) .

-   [Предварительные условия](#prerequisites)
-   [Классы C++, используемые в источнике MPEG-1](#c-classes-used-in-the-mpeg-1-source)
-   [Обработчик потока байтов](#byte-stream-handler)
-   [Дескриптор представления](#presentation-descriptor)
-   [Состояния потоковой передачи](#streaming-states)
    -   [Запуск](#start)
    -   [Пауза](#pause)
    -   [Остановить](#stop)
-   [Примеры запросов](#sample-requests)
-   [Конец потока](#end-of-stream)
-   [Асинхронные операции](#asynchronous-operations)
    -   [Очередь операций](#operation-queue)
-   [См. также](#related-topics)

## <a name="prerequisites"></a>Предварительные условия

Прежде чем читать этот раздел, необходимо ознакомиться со следующими концепциями Media Foundation:

-   [Объектная модель источника мультимедиа](media-source-object-model.md)
-   [Асинхронные методы обратного вызова](asynchronous-callback-methods.md).
-   [Рабочие очереди](work-queues.md)
-   [Генераторы событий мультимедиа](media-event-generators.md)
-   [Буферы мультимедиа](media-buffers.md)
-   [Примеры носителей](media-samples.md)
-   [Типы носителей](media-types.md)

Кроме того, необходимо иметь базовое представление об архитектуре Media Foundation, в частности роль источников мультимедиа в конвейере. (Дополнительные сведения см. в разделе [источники мультимедиа](media-sources.md).)

Кроме того, может потребоваться ознакомиться с разделом [Создание пользовательского источника мультимедиа](writing-a-custom-media-source.md), в котором приводятся более общие сведения о действиях, описанных здесь.

Этот раздел не позволяет воспроизвести весь код из примера пакета SDK, так как этот пример довольно большой.

## <a name="c-classes-used-in-the-mpeg-1-source"></a>Классы C++, используемые в источнике MPEG-1

Образец источника MPEG-1 реализуется со следующими классами C++:

-   `MPEG1ByteStreamHandler`. Реализует обработчик потока байтов для источника мультимедиа. При наличии потока байтов обработчик потока байтов создает экземпляр источника.
-   `MPEG1Source`. Реализует источник мультимедиа.
-   `MPEG1Stream`. Реализует объекты потока мультимедиа. Источник мультимедиа создает по одному `MPEG1Stream` объекту для каждого звукового или видеопотока в формате MPEG-1 битовый поток.
-   `Parser`. Выполняет синтаксический анализ битовый поток MPEG-1. В большинстве случаев сведения этого класса не относятся к Media Foundationным API.
-   Саурцеоп, Опкуеуе. Эти два класса управляют асинхронными операциями в источнике мультимедиа. (См. раздел [асинхронные операции](#asynchronous-operations)).

Другие вспомогательные классы описаны далее в разделе.

## <a name="byte-stream-handler"></a>Обработчик Byte-Stream

Обработчик *байтов потока* — это объект, который создает источник мультимедиа. Обработчик потока байтов создается исходным распознавателем. приложения не взаимодействуют напрямую с обработчиком потока байтов. Сопоставитель источника обнаруживает обработчик потока байтов, просматривая в реестре. Обработчик регистрируется по расширению имени файла или типу MIME. Для источника MPEG-1 обработчик потока байтов регистрируется для расширения имени файла ". mpg".

> [!Note]  
> Если требуется поддержка пользовательских схем URL-адресов, можно также написать *обработчик схемы*. Источник MPEG-1 предназначен для локальных файлов, а Media Foundation уже предоставляет обработчик схемы для URL-адресов "file://".

 

Обработчик потока байтов реализует интерфейс [**имфбитестреамхандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) . Этот интерфейс имеет два наиболее важных метода, которые должны быть реализованы:

-   [**Бегинкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). Запускает асинхронную операцию для создания источника мультимедиа.
-   [**Ендкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject). Завершает асинхронный вызов.

Два других метода являются необязательными и не реализуются в примере пакета SDK:

-   [**Канцелобжекткреатион**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation). Отменяет метод [**бегинкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) . Этот метод полезен для сетевого источника, который может иметь высокую задержку при запуске.
-   [**Жетмакснумберофбитесрекуиредфорресолутион**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution). Возвращает максимальное число байтов, которое обработчик будет считывать из исходного потока. Реализуйте этот метод, если известно, сколько данных обработчика потока байтов перед созданием источника мультимедиа. В противном случае просто возвратите **E \_ нотимпл**.

Ниже приведена реализация метода [**бегинкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) :


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



Метод выполняет следующие действия:

1.  Создает новый экземпляр объекта `MPEG1Source`.
2.  Создайте объект асинхронного результата. Этот объект используется позже для вызова метода обратного вызова распознавателя источника.
3.  Вызывает `MPEG1Source::BeginOpen` асинхронный метод, определенный в `MPEG1Source` классе.
4.  Устанавливает *ппиункновнканцелкукие* в **значение NULL**, которое информирует вызывающий объект о том, что [**канцелобжекткреатион**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) не поддерживается.

`MPEG1Source::BeginOpen`Метод выполняет фактическую работу по чтению потока байтов и инициализации `MPEG1Source` объекта. Этот метод не является частью общедоступного API. Можно определить любой механизм между обработчиком и источником мультимедиа, отвечающим вашим потребностям. Размещение большей части логики в источнике мультимедиа обеспечивает сравнительно простой обработчик потока байтов.

Вкратце, `BeginOpen` выполняет следующие действия:

1.  Вызывает [**имфбитестреам::-Capabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) , чтобы убедиться, что исходный байтовый поток доступен для чтения и поиска.
2.  Вызывает метод [**имфбитестреам:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) для запуска асинхронного запроса ввода-вывода.

Остальная часть инициализации выполняется асинхронно. Источник мультимедиа считывает из потока достаточно данных для синтаксического анализа заголовков последовательности MPEG-1. Затем создается *дескриптор представления*, который является объектом, используемым для описания потоков аудио и видео в файле. (Дополнительные сведения см. в разделе [дескриптор представления](#presentation-descriptor).) По `BeginOpen` завершении операции обработчик потока байтов вызывает метод обратного вызова распознавателя исходного кода. На этом этапе сопоставитель источника вызывает [**имфбитестреамхандлер:: ендкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject). Метод **ендкреатеобжект** возвращает состояние операции.


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



Если во время этого процесса возникает ошибка, обратный вызов вызывается с кодом состояния ошибки.

## <a name="presentation-descriptor"></a>Дескриптор представления

Дескриптор презентации описывает содержимое файла MPEG-1, включая следующие сведения:

-   Число потоков.
-   Формат каждого потока.
-   Идентификаторы потоков.
-   Состояние выбора каждого потока (выбрано или отменяется выбор).

В терминах архитектуры Media Foundation дескриптор презентации содержит один или несколько *дескрипторов потоков*. Каждый дескриптор потока содержит *обработчик типа мультимедиа*, который используется для получения или задания типов мультимедиа в потоке. Media Foundation предоставляет стандартные реализации дескриптора презентации и дескриптора потока; они подходят для большинства источников мультимедиа.

Чтобы создать дескриптор презентации, выполните следующие действия.

1.  Для каждого потока:
    1.  Укажите идентификатор потока и массив возможных типов носителей. Если поток поддерживает несколько типов носителей, упорядочивайте список типов мультимедиа по предпочтениям, если они есть. (Сначала укажите оптимальный тип, а последний — самый оптимальный тип.)
    2.  Вызовите [**мфкреатестреамдескриптор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) , чтобы создать дескриптор потока.
    3.  Вызовите [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) для только что созданного дескриптора потока.
    4.  Вызовите метод [**имфмедиатипехандлер:: сеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , чтобы задать формат по умолчанию для потока. Если имеется более одного типа мультимедиа, обычно следует задать первый тип в списке.
2.  Вызовите [**мфкреатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) и передайте массив указателей дескриптора потока.
3.  Для каждого потока вызовите [**имфпресентатиондескриптор:: селектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) или [**деселектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) , чтобы задать состояние выбора по умолчанию. Если имеется более одного потока одного типа (аудио или видео), по умолчанию должен быть выбран только один поток.

`MPEG1Source`Объект создает дескриптор представления в своем `InitPresentationDescriptor` методе:


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



Приложение получает дескриптор представления путем вызова [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Этот метод создает неполную копию дескриптора представления путем вызова [**имфпресентатиондескриптор:: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone). (Копия содержит указатели на исходные дескрипторы потока.) Приложение может использовать дескриптор презентации, чтобы задать тип мультимедиа, выбрать поток или отменить выбор потока.

При необходимости дескрипторы представления и дескрипторы потоков могут содержать атрибуты, предоставляющие дополнительные сведения об источнике. Список таких атрибутов см. в следующих разделах:

-   [Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
-   [Атрибуты дескриптора потока](stream-descriptor-attributes.md)

Один атрибут заслуживает особого упоминания: атрибут [**« \_ \_ Длительность MF PD**](mf-pd-duration-attribute.md) » содержит общую длительность источника. Установите этот атрибут, если вы уверены, что длительность находится впереди. Например, длительность может быть указана в заголовках файлов в зависимости от формата файла. Приложение может отобразить это значение или использовать его для задания индикатора выполнения или панели поиска.

## <a name="streaming-states"></a>Состояния потоковой передачи

Источник мультимедиа определяет следующие состояния.



| Состояние    | Описание                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| Запуск  | Источник принимает и обрабатывает примеры запросов.                                                               |
| Пауза   | Источник принимает запросы выборки, но не обрабатывает их. Запросы ставятся в очередь до запуска источника. |
| Остановлена. | Источник отклоняет запросы выборки.                                                                             |



 

### <a name="start"></a>Начать

Метод [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) запускает источник мультимедиа. Она принимает следующие параметры.

-   Дескриптор презентации.
-   Идентификатор GUID формата времени.
-   Начальное расположение.

Приложение должно получить дескриптор презентации, вызвав [**креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) в источнике. Нет определенного механизма для проверки дескриптора представления. Если в приложении указан неправильный дескриптор представления, результаты не будут определены.

Идентификатор GUID формата времени определяет способ интерпретации начальной должности. Стандартный формат — 100-наносекундных единиц (NS), обозначенный GUID \_ null. Каждый источник мультимедиа должен поддерживать 100-НС единиц. Кроме того, источник может поддерживать другие единицы времени, такие как номер кадра или код времени. Однако нет стандартного способа запросить источник мультимедиа список поддерживаемых форматов времени.

Начальное расположение задается как **пропвариант**, что позволяет использовать различные типы данных в зависимости от формата времени. Для 100-NS тип **пропвариант** является либо **VT \_ i8** , либо **VT \_ Empty**. Если **VT \_ i8**, **пропвариант** содержит начальную точку в 100-единицах NS. Значение **VT \_ Empty** имеет специальное значение "начать с текущей позиции".

Реализуйте метод [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) следующим образом:

1.  Проверить параметры и состояние:
    -   Проверьте наличие параметров **null** .
    -   Проверьте GUID формата времени. Если значение недопустимо, возвращается **\_ \_ неподдерживаемый \_ \_ Формат времени в MF E**.
    -   Проверьте тип данных **пропвариант** , в котором находится начальная координата.
    -   Проверьте начальную точку. Если значение недопустимо, возвращается **MF \_ E \_ инвалидрекуест**.
    -   Если работа источника была завершена, возвращайте ключ **\_ \_ завершения работы MF E**.
2.  Если на шаге 1 не возникает ошибки, поочередно помещает асинхронную операцию в очередь. Все после этого шага происходит в потоке рабочей очереди.
3.  Для каждого потока:
    1.  Убедитесь, что поток уже активен из предыдущего запроса на [**Запуск**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) .
    2.  Вызовите [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) , чтобы проверить, выбрано ли приложение или отменяет выбор потока.
    3.  Если выбранный ранее поток теперь не выбран, очистите все недоставленные образцы для этого потока.
    4.  Если поток активен, источник мультимедиа (не поток) отправляет одно из следующих событий:
        -   Он отправляет [меупдатедстреам](meupdatedstream.md) , если поток был ранее активен.
        -   В противном случае он отправляет [меневстреам](menewstream.md).

        Для обоих событий данные события являются [**имфмедиастреам**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) указателем для потока.
    5.  Если источник перезапускается из приостановленного состояния, возможны незавершенные запросы на выборку. Если да, доставьте их сейчас.
    6.  Если источник ищет новую точку, каждый объект потока отправляет событие [местреамсикед](mestreamseeked.md) . В противном случае каждый поток отправляет событие [местреамстартед](mestreamstarted.md) .
4.  Если источник ищет новую точку, источник мультимедиа отправляет событие [месаурцесикед](mesourceseeked.md) . В противном случае он отправляет событие [месаурцестартед](mesourcestarted.md) .

Если ошибка возникает в любой момент после шага 2, источник отправляет событие [месаурцестартед](mesourcestarted.md) с кодом ошибки. Это предупреждает приложение о том, что метод [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) завершился сбоем асинхронно.

В следующем коде показаны шаги 1 – 2.


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



Остальные шаги показаны в следующем примере:


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



### <a name="pause"></a>Пауза

Метод [**имфмедиасаурце::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) приостанавливает источник мультимедиа. Реализуйте этот метод следующим образом:

1.  Постановка асинхронной операции в очередь.
2.  Каждый активный поток отправляет событие [местреампаусед](mestreampaused.md) .
3.  Источник мультимедиа отправляет событие [месаурцепаусед](mesourcepaused.md) .

При приостановке, исходная очередь помещает запросы на выборку, не обрабатывая их. (См. [примеры запросов](#sample-requests).)

### <a name="stop"></a>Stop

Метод [**имфмедиасаурце:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) останавливает источник мультимедиа. Реализуйте этот метод следующим образом:

1.  Постановка асинхронной операции в очередь.
2.  Каждый активный поток отправляет событие [местреамстоппед](mestreamstopped.md) .
3.  Очистите все образцы в очереди и примеры запросов.
4.  Источник мультимедиа отправляет событие [месаурцестоппед](mesourcestopped.md) .

При остановке источник отклоняет все запросы к примерам.

Если источник остановлен во время выполнения запроса ввода-вывода, запрос ввода-вывода может завершиться после того, как источник войдет в остановленное состояние. В этом случае источник должен отменить результат этого запроса ввода-вывода.

## <a name="sample-requests"></a>Образец запросов

Media Foundation использовать модель *извлечения* , в которой конвейер запрашивает образцы из источника мультимедиа. Это отличается от модели, используемой DirectShow, в которой образцы источников push-уведомлений.

Чтобы запросить новый пример, Media Foundation конвейер вызывает метод [**имфмедиастреам:: рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). Этот метод принимает указатель **IUnknown** , представляющий объект *маркера* . Реализация объекта токена находится в вызывающем объекте; Он просто предоставляет вызывающему объекту способ для трассировки запросов выборки. Параметр token может также иметь **значение NULL**.

Предполагая, что источник использует асинхронные запросы ввода-вывода для чтения данных, создание примеров не будет синхронизировано с примерами запросов. Чтобы синхронизировать примеры запросов с примером создания, источник мультимедиа выполняет следующие действия:

1.  Маркеры запроса помещаются в очередь.
2.  При создании образцов они помещаются во вторую очередь.
3.  Источник мультимедиа завершает пример запроса, получая маркер запроса из первой очереди и пример из второй очереди.
4.  Источник мультимедиа отправляет событие Мемедиасампле. Событие содержит указатель на образец, а образец содержит указатель на маркер.

На следующей схеме показана связь между событием [мемедиасампле](memediasample.md) , образцом и маркером запроса.

![Диаграмма, показывающая мемедиасампле, и пример очереди, указывающий на имфсампле; имфсампле и очередь запросов указывают на IUnknown](images/mediasourceimpl01.png)

В примере источника MPEG-1 этот процесс реализуется следующим образом:

1.  Метод [**рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) помещает запрос в очередь FIFO.
2.  По мере завершения запросов ввода-вывода источник мультимедиа создает новые образцы и помещает их во вторую очередь FIFO. (Эта очередь имеет максимальный размер, чтобы предотвратить слишком далекое чтение источника.)
3.  Если обе эти очереди имеют по крайней мере один элемент (один запрос и один пример), источник мультимедиа завершает первый запрос из очереди запросов, отправляя первый пример из очереди.
4.  Для доставки примера объект потока (не исходный объект) отправляет событие [мемедиасампле](memediasample.md) .
    -   Данные события являются указателем на интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) образца.
    -   Если запрос включал маркер, присоедините маркер к образцу, установив атрибут [**\_ токена мфсампликстенсион**](mfsampleextension-token-attribute.md) в образце.

На этом этапе есть три возможности:

-   Существует еще один пример в очереди образцов, но нет соответствующего запроса.
-   Существует запрос, но нет примера.
-   Обе очереди пусты; нет примеров и запросов.

Если пример очереди пуст, источник проверяет конец потока (см. [конец потока](#end-of-stream)). В противном случае он запускает другой запрос ввода-вывода для данных. Если во время этого процесса возникает какая либо ошибка, поток отправляет событие [Миррор](meerror.md) .

В следующем коде реализуется метод [**имфмедиастреам:: рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) :


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



`DispatchSamples`Метод извлекает образцы из очереди образцов, сопоставляет их с ожидающими запросами выборки и помещает в очередь события [мемедиасампле](memediasample.md) :


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



`DispatchSamples`Метод вызывается в следующих случаях:

-   Внутри метода [**рекуестсампле**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .
-   При перезапуске источника мультимедиа из приостановленного состояния.
-   При завершении запроса ввода-вывода.

## <a name="end-of-stream"></a>Конец потока

Если поток больше не содержит данных и все образцы для этого потока были доставлены, объекты потока отправляют событие [миндофстреам](meendofstream.md) .

Когда все активные потоки будут выполнены, источник мультимедиа отправляет событие [миндофпресентатион](meendofpresentation.md) .

## <a name="asynchronous-operations"></a>Асинхронные операции

Возможно, самая сложная часть написания источника мультимедиа — понимание Media Foundation асинхронной модели.

Все методы в источнике мультимедиа, которые управляют потоковой передачей, являются асинхронными. В каждом случае метод выполняет некоторую начальную проверку, например проверку параметров. Затем источник отправляет оставшуюся часть работы в рабочую очередь. По завершении операции источник мультимедиа отправляет событие обратно вызывающему объекту через интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) источника мультимедиа. Поэтому важно понимать рабочие очереди.

Чтобы поместить элемент в рабочую очередь, можно вызвать либо [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) , либо [**мфпутворкитемекс**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). Источник MPEG-1 использует **мфпутворкитем**, но две функции выполняют одно и то же действие. Функция **мфпутворкитем** принимает следующие параметры:

-   Значение **типа DWORD** , идентифицирующее рабочую очередь. Вы можете создать частную рабочую очередь или использовать **\_ \_ \_ стандартную очередь обратного вызова мфасинк**.
-   Указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Этот интерфейс обратного вызова вызывается для выполнения работы.
-   Необязательный объект состояния, который должен реализовывать **IUnknown**.

Рабочая очередь обслуживается одним или несколькими рабочими потоками, которые постоянно извлекают следующий рабочий элемент из очереди и вызывают метод [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) интерфейса обратного вызова.

Рабочие элементы не гарантированно выполняются в том же порядке, в котором они были помещены в очередь. Помните, что несколько потоков могут обслуживать одну и ту же рабочую очередь, поэтому вызовы [**вызова**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) могут перекрываться или происходить в неопределенном порядке. Таким образом, источник мультимедиа должен поддерживать правильное внутреннее состояние путем отправки элементов рабочей очереди в правильном порядке. При выполнении предыдущей операции источник начинает следующую операцию.

Для представления ожидающих операций источник MPEG-1 определяет класс с именем `SourceOp` :


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



`Operation`Перечисление определяет, какая операция находится в состоянии ожидания. Класс также содержит **пропвариант** для передачи дополнительных данных для операции.

### <a name="operation-queue"></a>Очередь операций

Для сериализации операций источник мультимедиа поддерживает очередь `SourceOp` объектов. Для управления очередью используется вспомогательный класс:


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



`OpQueue`Класс предназначен для наследования компонентом, выполняющим асинхронные рабочие элементы. Параметр *шаблона \_ типа Op* — это тип объекта, используемый для представления рабочих элементов в очереди. в данном случае *\_ типом Op* будет `SourceOp` . `OpQueue`Класс реализует следующие методы:

-   `QueueOperation` помещает новый элемент в очередь.
-   `ProcessQueue` отправляет следующую операцию из очереди. Этот метод является асинхронным.
-   `ProcessQueueAsync` Завершает асинхронный `ProcessQueue` метод.

Производным классом должен быть реализован еще два метода:

-   `ValidateOperation` проверяет, является ли он допустимым для выполнения указанной операции с учетом текущего состояния источника мультимедиа.
-   `DispatchOperation` выполняет асинхронный рабочий элемент.

Очередь операций используется следующим образом:

1.  Конвейер Media Foundation вызывает асинхронный метод в источнике мультимедиа, например [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  Асинхронный метод вызывает `QueueOperation` , который помещает [**начальную**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) операцию в очередь и вызывает `ProcessQueue` (в форме `SourceOp` объекта).
3.  `ProcessQueue` вызывает [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).
4.  Поток рабочей очереди вызывает `ProcessQueueAsync` .
5.  `ProcessQueueAsync`Метод вызывает `ValidateOperation` и `DispatchOperation` .

Следующий код помещает новую операцию в источник MPEG-1:


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



Следующий код обрабатывает очередь:


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



`ValidateOperation`Метод проверяет, может ли источник MPEG-1 отправлять следующую операцию в очереди. Если выполняется другая операция, `ValidateOperation` возвращает **MF \_ E \_ нотакцептинг**. Это гарантирует, что `DispatchOperation` при наличии другой ожидающей операции она не вызывается.


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



Метод DispatchOperation переключается по типу операции:


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



Подведение итогов.

1.  Конвейер вызывает асинхронный метод, например [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  Асинхронный метод вызывает `OpQueue::QueueOperation` , передавая указатель на `SourceOp` объект.
3.  `QueueOperation`Метод помещает операцию в очередь *\_ опкуеуе m* и вызывает `OpQueue::ProcessQueue` .
4.  `ProcessQueue`Метод вызывает [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem). С этого момента все происходит в Media Foundation потоке рабочей очереди. Асинхронный метод возвращает вызывающему объекту.
5.  Поток рабочей очереди вызывает `OpQueue::ProcessQueueAsync` метод.
6.  `ProcessQueueAsync`Метод вызывает `MPEG1Source:ValidateOperation` для проверки операции.
7.  `ProcessQueueAsync`Метод вызывает `MPEG1Source::DispatchOperation` для обработки операции.

Эта схема имеет несколько преимуществ.

-   Методы являются асинхронными, поэтому они не блокируют поток вызывающего приложения.
-   Операции отправляются в поток рабочих очередей Media Foundation, который совместно используется компонентами конвейера. Таким образом, источник мультимедиа не создает собственный поток, уменьшая общее количество создаваемых потоков.
-   Источник мультимедиа не блокируется при ожидании завершения операций. Это снижает вероятность того, что источник мультимедиа случайным образом вызовет взаимоблокировку и помогает сократить переключение контекста.
-   Источник мультимедиа может использовать асинхронный ввод-вывод для чтения исходного файла (путем вызова [**имфбитестреам:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)). Источник мультимедиа не требуется блокировать при ожидании завершения подпрограммы ввода-вывода.

Если следовать шаблону, показанному в примере пакета SDK, вы можете сосредоточиться на конкретных деталях источника мультимедиа.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Источники мультимедиа](media-sources.md)
</dt> <dt>

[Запись пользовательского источника мультимедиа](writing-a-custom-media-source.md)
</dt> </dl>

 

 



