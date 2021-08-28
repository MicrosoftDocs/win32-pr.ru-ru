---
description: В этом разделе описывается создание топологии для воспроизведения звука или видео.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Создание топологий воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563fcef0c9ba8b1a4a33aefc17c5cea744f051470bb04df0ab4699ed4af6fa8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600824"
---
# <a name="creating-playback-topologies"></a>Создание топологий воспроизведения

В этом разделе описывается создание топологии для воспроизведения звука или видео. Для базового воспроизведения можно создать частичную топологию, в которой исходные узлы подключены непосредственно к выходным узлам. Нет необходимости вставлять узлы для промежуточных преобразований, например декодеров или цветовых преобразователей. Сеанс мультимедиа будет использовать загрузчик топологии для разрешения топологии, а загрузчик топологии будет вставлять необходимые преобразования.

-   [Создание топологии](#creating-the-topology)
-   [подключение Потоки к приемникам мультимедиа](#connecting-streams-to-media-sinks)
-   [Создание приемника мультимедиа](#creating-the-media-sink)
-   [Следующие шаги](#next-steps)
-   [Связанные темы](#related-topics)

## <a name="creating-the-topology"></a>Создание топологии

Ниже приведены общие шаги для создания топологии частичного воспроизведения из источника мультимедиа.

1.  Создайте источник мультимедиа. В большинстве случаев для создания источника мультимедиа будет использоваться сопоставитель источников. Дополнительные сведения см. в разделе [сопоставитель источников](source-resolver.md).
2.  Получение дескриптора презентации источника мультимедиа.
3.  Создайте пустую топологию.
4.  Используйте дескриптор представления для перечисления дескрипторов потоков. Для каждого дескриптора потока:
    1.  Получение основного типа носителя потока, например аудио или видео.
    2.  Проверьте, выбран ли поток в данный момент. (При необходимости можно выбрать или отменить выбор потока в зависимости от типа носителя.)
    3.  Если выбран поток, создайте объект активации для приемника мультимедиа на основе типа носителя потока.
    4.  Добавьте исходный узел для потока и выходной узел для приемника мультимедиа.
    5.  Подключение исходный узел в выходной узел.

Чтобы упростить этот процесс, пример кода в этом разделе состоит из нескольких функций. Функция верхнего уровня называется `CreatePlaybackTopology` . Он принимает три параметра:

-   Указатель на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) источника мультимедиа.
-   Указатель на интерфейс [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) дескриптора презентации. Получите этот указатель, вызвав [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Для источников с несколькими презентациями дескрипторы представления для последующих презентаций доставляются в событии [меневпресентатион](menewpresentation.md) .
-   Маркер окна приложения. Если источник содержит видео-поток, в этом окне будет показано видео.

Функция возвращает указатель на топологию частичного воспроизведения в параметре *пптопологи* .


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



Эта функция выполняет следующие действия:

1.  Вызовите [**мфкреатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) , чтобы создать топологию. Изначально топология не содержит узлов.
2.  Вызовите метод [**имфпресентатиондескриптор:: жетстреамдескрипторкаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) , чтобы получить количество потоков в презентации.
3.  Для каждого потока вызовите функцию, определяемую приложением, `AddBranchToPartialTopology` в ветвь в топологии. Эта функция показана в следующем разделе.

## <a name="connecting-streams-to-media-sinks"></a>подключение Потоки к приемникам мультимедиа

Для каждого выбранного потока добавьте исходный узел и выходной узел, а затем соедините два узла. Исходный узел представляет поток. Выходной узел представляет либо Расширенный модуль [подготовки видео](enhanced-video-renderer.md) (Евр), либо [потоковый рендеринг звука](streaming-audio-renderer.md) (САР).

`AddBranchToPartialTopology`Функция, показанная в следующем примере, принимает следующие параметры:

-   Указатель на интерфейс [**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) топологии.
-   Указатель на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) источника мультимедиа.
-   Указатель на интерфейс [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) дескриптора презентации.
-   Отсчитываемый от нуля индекс потока.
-   Маркер окна видео. Этот обработчик используется только для потока видео.


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



Функция выполняет следующие действия:

1.  Вызывает [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) и передает потоковый индекс. Этот метод возвращает указатель на дескриптор потока для этого потока, а также логическое значение, указывающее, выбран ли поток.
2.  Если поток не выбран, функция завершает работу и возвращает значение S \_ ОК, поскольку приложению не нужно создавать ветвь топологии для потока, если она не выбрана.
3.  Если выбран поток, функция завершает ветвь Topology следующим образом:
    1.  Создает объект активации для приемника, вызывая определяемую приложением функцию Креатемедиасинкактивате. Эта функция показана в следующем разделе.
    2.  Добавляет в топологию исходный узел. Код для этого шага показан в разделе [Создание исходных узлов](creating-source-nodes.md).
    3.  Добавляет выходной узел в топологию. Код для этого шага показан в разделе [Создание выходных узлов](creating-output-nodes.md).
    4.  Подключает два узла путем вызова [**имфтопологиноде:: коннектаутпут**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) на исходном узле. Подключив узлы, приложение указывает, что вышестоящий узел должен доставлять данные в подчиненный узел. Исходный узел имеет один выход, а выходной узел имеет один вход, поэтому оба индекса потоков равны нулю.

Более сложные приложения могут выбирать или отменять выбор потоков вместо использования конфигурации по умолчанию источника. Источник может иметь несколько потоков, и все они могут быть выбраны по умолчанию. Дескриптор представления источника мультимедиа имеет набор по умолчанию для выбора потоков. В простом видеофайле с одним звуковым потоком и видеопотоком источник мультимедиа обычно выбирает оба потока по умолчанию. Однако файл может иметь несколько звуковых потоков для разных языков или несколько видеопотоков, закодированных с разной скоростью. В этом случае некоторые из потоков будут отделяться по умолчанию. Приложение может изменить выбор, вызвав [**имфпресентатиондескриптор:: селектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) и [**Имфпресентатиондескриптор::D еселектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) в дескрипторе презентации.

## <a name="creating-the-media-sink"></a>Создание приемника мультимедиа

Следующая функция создает объект активации для приемника мультимедиа Евр или САР.


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



Эта функция выполняет следующие действия:

1.  Вызывает [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) в дескрипторе потока. Этот метод возвращает указатель интерфейса [**имфмедиатипехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .

2.  Вызывает [**имфмедиатипехандлер:: жетмажортипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Этот метод возвращает идентификатор GUID основного типа для потока.

3.  Если тип потока — Audio, функция вызывает [**мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) для создания объекта активации модуля подготовки звука. Если тип потока — Video, функция вызывает [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) для создания объекта активации модуля обработки видео. Обе эти функции возвращают указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Этот указатель используется для инициализации выходного узла для приемника, как показано выше.

Для любого другого типа потока этот пример возвращает код ошибки. Кроме того, можно просто отменить выбор потока.

## <a name="next-steps"></a>Дальнейшие действия

Чтобы воспроизвести один файл мультимедиа за раз, необходимо поставить в очередь топологию в сеансе мультимедиа, вызвав [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology). Сеанс мультимедиа будет использовать загрузчик топологии для разрешения топологии. Полный пример см. в разделе [Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Как воспроизвести незащищенные файлы мультимедиа](how-to-play-unprotected-media-files.md)
</dt> <dt>

[Сеанс мультимедиа](media-session.md)
</dt> <dt>

[Топологий](topologies.md)
</dt> </dl>

 

 



