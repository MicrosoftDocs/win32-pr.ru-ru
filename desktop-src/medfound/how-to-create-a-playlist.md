---
description: В этом разделе описывается использование источника последовательности для воспроизведения последовательности файлов.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Создание списка воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e6e19766c3fa569a701fea9bed0f05d11a4324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543610"
---
# <a name="how-to-create-a-playlist"></a>Создание списка воспроизведения

В этом разделе описывается использование источника последовательности для воспроизведения последовательности файлов.

## <a name="overview"></a>Обзор

Чтобы воспроизвести файлы мультимедиа в последовательности, приложение должно добавить топологии в последовательность для создания списка воспроизведения и поставить эти топологии в сеансе мультимедиа для воспроизведения.

Источник Sequencer обеспечивает эффективное воспроизведение, инициализируя и загружая следующую топологию, прежде чем сеанс мультимедиа начнет воспроизводить текущую топологию. Это позволяет приложению быстро запускать следующую топологию при необходимости.

Сеанс мультимедиа отвечает за передачу данных в приемники и воспроизведение топологий в источнике последовательности. Кроме того, сеанс мультимедиа управляет временем презентации для сегментов.

Дополнительные сведения о том, как источник Sequencer управляет топологиями, см. [в разделе сведения о источнике Sequencer](about-the-sequencer-source.md).

В этом пошаговом руководстве содержатся следующие шаги.

1.  [Предварительные условия](#prerequisites)
2.  [Инициализация Media Foundation](#initializing-media-foundation)
3.  [Создание объектов Media Foundation](#creating-media-foundation-objects)
4.  [Создание источника мультимедиа](#creating-the-media-source)
5.  [Создание частичных топологий](#creating-partial-topologies)
6.  [Добавление топологий в источник Sequencer](#adding-topologies-to-the-sequencer-source)
7.  [Настройка первой топологии в сеансе мультимедиа](#setting-the-first-topology-on-the-media-session)
8.  [Постановка следующей топологии в очередь в сеансе мультимедиа](#queuing-the-next-topology-on-the-media-session)
9.  [Освобождение источника Sequencer](#releasing-the-sequencer-source)

Приведенные в этом разделе примеры кода являются выдержками из [исходного примера программы Sequencer](sequencer-source-example-code.md), который содержит полный код примера.

## <a name="prerequisites"></a>Предварительные условия

Перед началом этого пошагового руководства ознакомьтесь со следующими концепциями Media Foundation:

-   [Сеанс мультимедиа](media-session.md)
-   [Топологии](topologies.md)
-   [Генераторы событий мультимедиа](media-event-generators.md)
-   [Дескрипторы представления](presentation-descriptors.md)

Также прочитайте [о том, как воспроизводить файлы мультимедиа с помощью Media Foundation](how-to-play-unprotected-media-files.md), так как пример кода, Швон здесь, расширяется по коду в этом разделе.

## <a name="initializing-media-foundation"></a>Инициализация Media Foundation

Прежде чем можно будет использовать любые Media Foundation интерфейсы или методы, инициализируйте Media Foundation, вызвав функцию [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) . Дополнительные сведения см. в разделе [инициализация Media Foundation](initializing-media-foundation.md).


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a>Создание объектов Media Foundation

Затем создайте следующие объекты Media Foundation:

-   Сеанс мультимедиа. Этот объект предоставляет интерфейс [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) , который предоставляет методы для воспроизведения, приостановки и остановки текущей топологии.
-   Источник Sequencer. Этот объект предоставляет интерфейс [**имфсекуенцерсаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) , который предоставляет методы для добавления, обновления и удаления топологий в последовательности.

1.  Чтобы создать сеанс мультимедиа, вызовите функцию [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) .
2.  Вызовите метод [**имфмедиаевенткуеуе:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) , чтобы запросить первое событие из сеанса мультимедиа.
3.  Вызовите функцию [**мфкреатесекуенцерсаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) , чтобы создать источник Sequencer.

Следующий код создает сеанс мультимедиа и запрашивает первое событие:


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a>Создание источника мультимедиа

Затем создайте источник мультимедиа для первого сегмента списка воспроизведения. Используйте [сопоставитель источников](source-resolver.md) для создания источника мультимедиа на основе URL-адреса. Для этого вызовите функцию [**мфкреатесаурцересолвер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) , чтобы создать сопоставитель источника, а затем вызовите метод [**Имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) , чтобы создать источник мультимедиа.

Сведения об источниках мультимедиа см. в статье [источники мультимедиа](media-sources.md).

## <a name="creating-partial-topologies"></a>Создание частичных топологий

Каждый сегмент в источнике Sequencer имеет собственную частичную топологию. Затем создайте частичные топологии для источников мультимедиа. Для частичной топологии исходные узлы топологии напрямую соединяются с выходными узлами без указания промежуточных преобразований. Сеанс мультимедиа использует объект Loader Topology для разрешения топологии. После разрешения топологии добавляются необходимые декодеры и другие узлы преобразования. Источник Sequencer также может содержать полные топологии.

Чтобы создать объект Topology, используйте функцию [**мфкреатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) , а затем используйте интерфейс [**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) для создания узлов потоков.

Полные инструкции по использованию этих программных элементов для создания топологий см. в разделе [Создание топологий воспроизведения](creating-playback-topologies.md).

Приложение может воспроизвести выбранную часть исходного кода, настроив исходный узел. Для этого задайте атрибут [**MF \_ топоноде \_ Медиастарт**](mf-toponode-mediastart-attribute.md) и атрибут [**MF \_ Топоноде \_ медиастоп**](mf-toponode-mediastop-attribute.md) в **\_ \_ \_ узле** топология MF в топологии с саурцестреам узлами. Укажите время начала и время окончания работы носителя относительно начала исходного источника как типы **UINT64** .

## <a name="adding-topologies-to-the-sequencer-source"></a>Добавление топологий в источник Sequencer

Затем добавьте к источнику Sequencer созданные разделяемые топологии. Каждому элементу последовательности, называемому *сегментом*, присваивается идентификатор **мфсекуенцерелементид** . Дополнительные сведения о том, как источник Sequencer управляет топологиями, см. [в разделе сведения о источнике Sequencer](about-the-sequencer-source.md).

После добавления всех топологий в источник Sequencer приложение должно отметить последний сегмент в последовательности для завершения воспроизведения в конвейере. Без этого флага источник Sequencer требует добавления дополнительных топологий.

1.  Вызовите метод [**имфсекуенцерсаурце:: аппендтопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) , чтобы добавить определенную топологию в источник Sequencer.

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    [**Аппендтопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) добавляет указанную топологию в последовательность. Этот метод возвращает идентификатор сегмента в параметре *пдвид* .

    Если топология является последней в источнике Sequencer, передайте Секуенцертопологифлагс \_ последним в параметре *dwFlags* . Это значение определено в перечислении [**мфсекуенцертопологифлагс**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) .

2.  Вызовите [**имфсекуенцерсаурце:: упдатетопологифлагс**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) , чтобы обновить флаги топологии, связанной с идентификатором сегмента во входном списке. В этом случае вызов указывает, что указанный сегмент является последним сегментом в секвенсоре. (Этот вызов необязателен, если последняя топология указана в вызове [**аппендтопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) .)

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

Приложение может заменить топологию сегмента другой топологией, вызвав метод [**имфсекуенцерсаурце:: упдатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) и передав новую топологию в *птопологи*. Если в новой топологии есть новые собственные источники, источники добавляются в исходный кэш. Список предустановленного обновления также обновляется.

## <a name="setting-the-first-topology-on-the-media-session"></a>Настройка первой топологии в сеансе мультимедиа

Затем поочередно ставить первую топологию в источнике последовательности в сеансе мультимедиа. Чтобы получить первую топологию из источника Sequencer, приложение должно вызвать метод [**имфмедиасаурцетопологипровидер:: жетмедиасаурцетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) . Этот метод возвращает частичную топологию, которая разрешается сеансом мультимедиа.

Сведения о частичной топологии см. в разделе [о топологиях](about-topologies.md).

1.  Получите собственный источник мультимедиа для первой топологии источника последовательности.
2.  Создайте дескриптор представления для источника мультимедиа, вызвав метод [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .
3.  Получите связанную топологию для презентации, вызвав метод [**имфмедиасаурцетопологипровидер:: жетмедиасаурцетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .
4.  Установите первую топологию в сеансе мультимедиа, вызвав [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

    Вызовите [**сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) , указав для параметра *двсеттопологифлагс* значение **null**. Это указывает сеансу мультимедиа запустить указанную топологию по завершении текущей топологии. Так как в этом случае указанная топология является первой, а текущая презентация отсутствует, сеанс мультимедиа запускает новую презентацию немедленно.

    Значение **null** также указывает на то, что сеанс мультимедиа должен разрешить топологию, так как топология, возвращаемая поставщиком топологии, всегда является частичной топологией.


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



## <a name="queuing-the-next-topology-on-the-media-session"></a>Постановка следующей топологии в очередь в сеансе мультимедиа

Затем приложению необходимо выполнить обработку события [меневпресентатион](menewpresentation.md) .

Источник Sequencer вызывает [меневпресентатион](menewpresentation.md) , когда сеанс мультимедиа начинает воспроизводить сегмент с другим сегментом после него. Это событие информирует приложение о следующей топологии в источнике последовательности, предоставляя дескриптор представления для следующего сегмента в списке предподготовки. Приложение должно получить связанную топологию с помощью поставщика топологии и поместить его в очередь в сеансе мультимедиа. Затем источник Sequencer выполняет откат этой топологии, что обеспечивает простой переход между презентациями.

Когда приложение выполняет поиск по сегментам, приложение получает несколько событий [меневпресентатион](menewpresentation.md) , так как источник Sequencer обновляет предварительную отрезку и настраивает правильную топологию. Приложение должно выполнить обработку каждого события и поставить в очередь топологию, возвращенную в данных события, в сеансе мультимедиа. Дополнительные сведения о пропущенных сегментах см. [в разделе Использование источника Sequencer](using-the-sequencer-source.md).

Дополнительные сведения о получении уведомлений об источниках Sequencer см. в статье [источники событий Sequencer](sequencer-source-events.md).

1.  В обработчике событий [меневпресентатион](menewpresentation.md) извлеките дескриптор представления для следующего сегмента из данных события.
2.  Получите связанную топологию для презентации, вызвав метод [**имфмедиасаурцетопологипровидер:: жетмедиасаурцетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .
3.  Задайте топологию в сеансе мультимедиа, вызвав метод [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) .

    Сеанс мультимедиа запускает новую презентацию после завершения текущей презентации.


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a>Освобождение источника Sequencer

Наконец, завершите работу источника Sequencer. Для этого вызовите метод [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) в источнике Sequencer. Этот вызов завершает работу всех базовых исходных источников мультимедиа в источнике Sequencer.

После освобождения источника Sequencer приложение должно закрыть и завершить сеанс мультимедиа, вызвав [**имфмедиасессион:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) и [**Имфмедиасессион:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)в этом порядке.

Чтобы избежать утечек памяти, приложение должно освободить указатели на Media Foundation интерфейсы, когда они больше не нужны.

## <a name="next-steps"></a>Next Steps

В этом пошаговом руководстве показано, как создать базовый список воспроизведения с помощью источника Sequencer. После создания списка воспроизведения может потребоваться добавить дополнительные функции, такие как пропуск сегмента, изменение состояния воспроизведения и поиск в сегменте. В следующем списке приведены ссылки на соответствующие разделы.

-   [Управление состояниями представления](how-to-control-presentation-states.md). источник Sequencer использует сеанс мультимедиа для обеспечения управления транспортом, например воспроизведения, паузы и остановки.
-   [Выполнение очистки](how-to-perform-scrubbing.md) описывает шаги, необходимые для поиска определенной позицией в потоке.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Источник Sequencer](sequencer-source.md)
</dt> </dl>

 

 



