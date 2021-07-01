---
description: В этой статье описывается, как написать пользовательский объект Presenter для расширенного модуля подготовки видео (Евр).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Написание выступающего Евр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505ba7ec225ac5f1316ad4343a4e1058ff0b6cb8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118779"
---
# <a name="how-to-write-an-evr-presenter"></a>Написание выступающего Евр

В этой статье описывается, как написать пользовательский объект Presenter для расширенного модуля подготовки видео (Евр). Пользовательский выступающий может использоваться как в DirectShow, так и в Media Foundation; интерфейсы и объектная модель одинаковы для обеих технологий, хотя точная последовательность операций может отличаться.

Пример кода в этом разделе адаптируется из [образца еврпресентер](evrpresenter-sample.md), который предоставляется в Windows SDK.

В этом разделе содержатся следующие подразделы.

-   [Предварительные требования](#prerequisites)
-   [Объектная модель Presenter](#presenter-object-model)
    -   [Поток данных внутри Евр](#data-flow-inside-the-evr)
    -   [Состояния выступающих](#presenter-states)
    -   [Интерфейсы выступающих](#presenter-interfaces)
    -   [Реализация Имфвидеодевицеид](#implementing-imfvideodeviceid)
    -   [Реализация Имфтопологисервицелукупклиент](#implementing-imftopologyservicelookupclient)
    -   [Реализация Имфвидеопресентер](#implementing-imfvideopresenter)
    -   [Реализация Имфклоккстатесинк](#implementing-imfclockstatesink)
    -   [Реализация Имфратесуппорт](#implementing-imfratesupport)
    -   [Отправка событий в Евр](#sending-events-to-the-evr)
-   [Форматы согласования](#negotiating-formats)
-   [Управление устройством Direct3D](#managing-the-direct3d-device)
    -   [Выделение поверхностей Direct3D](#allocating-direct3d-surfaces)
    -   [Примеры. Отслеживание](#tracking-samples)
-   [Обработка выходных данных](#processing-output)
    -   [Перерисовка кадров](#repainting-frames)
    -   [Примеры планирования](#scheduling-samples)
    -   [Представление образцов](#presenting-samples)
    -   [Исходный и конечный прямоугольники](#source-and-destination-rectangles)
    -   [Конец потока](#end-of-stream)
-   [Пошаговое выполнение кадра](#frame-stepping)
    -   [Реализация пошагового выполнения кадра](#implementing-frame-stepping)
-   [Установка параметра Presenter в Евр](#setting-the-presenter-on-the-evr)
    -   [Настройка выступающего в DirectShow](#setting-the-presenter-in-directshow)
    -   [Настройка выступающего в Media Foundation](#setting-the-presenter-in-media-foundation)
-   [Связанные темы](#related-topics)

## <a name="prerequisites"></a>Предварительные требования

Перед написанием пользовательского Presenter необходимо ознакомиться со следующими технологиями:

-   Расширенный модуль подготовки видео. См. [Расширенный модуль подготовки видео](enhanced-video-renderer.md).
-   Графическая система Direct3D. Для написания выступающего не нужно понимать трехмерную графику, но вам необходимо знать, как создать устройство Direct3D и управлять областями Direct3D. Если вы не знакомы с Direct3D, ознакомьтесь с разделами "устройства Direct3D" и "ресурсы Direct3D" в документации по DirectX Graphics SDK.
-   Графы фильтров DirectShow или конвейер Media Foundation в зависимости от того, какая технология будет использоваться приложением для визуализации видео.
-   [Преобразования Media Foundation](media-foundation-transforms.md). Микшер Евр является Media Foundation преобразованием, а выступающий вызывает методы непосредственно в микшере.
-   Реализация COM-объектов. Выступающий — это внутрипроцессный COM-объект с произвольным потоком.

## <a name="presenter-object-model"></a>Объектная модель Presenter

В этом разделе содержится обзор объектной модели и интерфейсов Presenter.

### <a name="data-flow-inside-the-evr"></a>Поток данных внутри Евр

Евр использует два подключаемых компонента для отрисовки видео: *микшер* и *Presenter*. Микшер смешивает видеопотокы и при необходимости разменяет видео. Выступающий рисует (или *представляет*) видео на экране и планируется при прорисовке каждого кадра. Приложения могут заменить любой из этих объектов пользовательской реализацией.

Евр имеет один или несколько входных потоков, а микшер имеет соответствующее количество входных потоков. Поток 0 всегда является *ссылочным потоком*. Другие потоки — это *подпотоки*, которые микшер альфа-смешивается на поток ссылок. Ссылочный поток определяет ставку основного кадра для композитного видео. Для каждого опорного кадра микшер принимает самый последний кадр из каждого подпотока, альфа-смешение их со ссылочным кадром и выводит один составной кадр. Микшер также выполняет дечередование и преобразование цветов из YUV в RGB при необходимости. Евр всегда вставляет микшер в видеоконвейер, независимо от числа входных потоков или формата видео. Этот процесс показан на следующем рисунке.

![Схема, показывающая поток ссылок и подпоток, указывающий микшер, указывающий на выступающий, указывающий на дисплей](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

Выступающий выполняет следующие задачи:

-   Задает формат вывода для микшера. Перед началом потоковой передачи, выступающий задает тип мультимедиа в выходном потоке микшера. Этот тип мультимедиа определяет формат составного изображения.
-   Создает устройство Direct3D.
-   Выделяет поверхности Direct3D. Микшер блитс составные кадры на эти поверхности.
-   Возвращает выходные данные микшера.
-   Планирует, когда отображаются кадры. Евр предоставляет часы презентации, и выступающие планирует кадры в соответствии с этим часами.
-   Представляет каждый кадр с помощью Direct3D.
-   Выполняет пошаговое выполнение и очистку кадра.

### <a name="presenter-states"></a>Состояния выступающих

В любое время выступающий находится в одном из следующих состояний:

-   *Запущено*. Часы презентации Евр. Выступающие планирует видеоматериалы для представления по мере их прибытия.
-   *Приостановлено*. Часы презентации приостановлены. В выступающих отсутствуют новые образцы, но хранится очередь запланированных выборок. Если поступают новые образцы, они добавляются в очередь.
-   *Остановлен*. Часы презентации остановлены. Выступающий отклоняет все запланированные выборки.
-   *Завершение работы*. Выступающие освобождает все ресурсы, связанные с потоковой передачей, например, поверхности Direct3D. Это начальное состояние выступающего и конечное состояние до уничтожения выступающего.

В примере кода в этом разделе Состояние выступающего представлено перечислением:


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



Некоторые операции недопустимы, пока выступающий находится в состоянии завершения работы. Пример кода проверяет это состояние, вызывая вспомогательный метод:


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a>Интерфейсы выступающих

Для реализации следующих интерфейсов требуется выступающий.



| Интерфейс                                                                | Описание                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**имфклоккстатесинк**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | Уведомляет выступающий, когда изменяется состояние часов Евр. См. раздел [Реализация имфклоккстатесинк](#implementing-imfclockstatesink).                                   |
| [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | Предоставляет приложению и другим компонентам конвейера способ получения интерфейсов от выступающего.                                                       |
| [**имфтопологисервицелукупклиент**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Позволяет ведущему получать интерфейсы от Евр или микшера. См. раздел [Реализация имфтопологисервицелукупклиент](#implementing-imftopologyservicelookupclient). |
| [**имфвидеодевицеид**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Гарантирует, что выступающий и микшер используют совместимые технологии. См. раздел [Реализация имфвидеодевицеид](#implementing-imfvideodeviceid).                          |
| [**имфвидеопресентер**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | Обрабатывает сообщения от Евр. См. раздел [Реализация имфвидеопресентер](#implementing-imfvideopresenter).                                                             |



 

Следующие интерфейсы являются необязательными:



| Интерфейс                                                | Описание                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иевртрустедвидеоплугин**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Позволяет ведущему работать с защищенным носителем. Реализуйте этот интерфейс, если ваш Presenter является доверенным компонентом, предназначенным для работы в защищенном пути носителя (PMP). |
| [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Сообщает диапазон скорости воспроизведения, поддерживаемый выступающим. См. раздел [Реализация имфратесуппорт](#implementing-imfratesupport).                                         |
| [**имфвидеопоситионмаппер**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Сопоставляет координаты на выходном видеокадре с координатами на входном видеокадре.                                                                                       |
| [**икуалпроп**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | Сообщает сведения о производительности. Евр использует эти сведения для управления качеством. Этот интерфейс описан в пакете SDK для DirectShow.                        |



 

Вы также можете предоставить интерфейсы для приложения для взаимодействия с выступающим. Для этой цели в стандартном выступающем реализуется интерфейс [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) . Вы можете реализовать этот интерфейс или определить собственный. Приложение получает интерфейсы от Presenter, вызывая [**имфжетсервице::**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Евр в. Если идентификатор GUID службы **MR_VIDEO_RENDER_SERVICE**, ЕВР **передает запрос на** выступающий.

### <a name="implementing-imfvideodeviceid"></a>Реализация Имфвидеодевицеид

Интерфейс [**имфвидеодевицеид**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) содержит один метод [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), который возвращает GUID устройства. GUID устройства гарантирует, что выступающий и микшер используют совместимые технологии. Если идентификаторы GUID устройства не совпадают, инициализация Евр не выполняется.

Стандартный микшер и настоящее устройство используют Direct3D 9 с идентификатором GUID устройства, равным **IID_IDirect3DDevice9**. Если вы планируете использовать пользовательский объект Presenter со стандартным микшером, то GUID устройства должен быть **IID_IDirect3DDevice9**. При замене обоих компонентов можно определить новый GUID устройства. В оставшейся части этой статьи предполагается, что в выступающих используется Direct3D 9. Ниже приведена стандартная реализация [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid).


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



Метод должен быть выполнен, даже когда выступающий завершает работу.

### <a name="implementing-imftopologyservicelookupclient"></a>Реализация Имфтопологисервицелукупклиент

Интерфейс [**имфтопологисервицелукупклиент**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) позволяет ведущему получать указатели интерфейса из Евр и из микшера следующим образом:

1.  Когда Евр инициализирует выступающий, он вызывает метод [**имфтопологисервицелукупклиент:: инитсервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) выступающего. Аргумент является указателем на интерфейс [**ИМФТОПОЛОГИСЕРВИЦЕЛУКУП**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) Евр.
2.  Выступающий вызывает [**имфтопологисервицелукуп:: лукупсервице**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) , чтобы получить указатели интерфейса из Евр или микшера.

Метод [**лукупсервице**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) аналогичен методу [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) . Оба метода принимают в качестве входных данных идентификатор GUID службы и идентификатор интерфейса (IID), но **лукупсервице** возвращает массив указателей интерфейса, а функция- **службы** возвращает один указатель. Однако на практике размер массива всегда можно задать равным 1. Запрашиваемый объект зависит от идентификатора GUID службы:

-   Если идентификатор GUID службы — **MR_VIDEO_RENDER_SERVICE**, ЕВР запрашивается.
-   Если идентификатор GUID службы — **MR_VIDEO_MIXER_SERVICE**, запрашивается микшер.

В реализации [**инитсервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)получите следующие интерфейсы из Евр:



| Интерфейс Евр                                | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**имедиаевентсинк**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | Предоставляет выступающий способ отправки сообщений в Евр. Этот интерфейс определен в пакете SDK DirectShow, поэтому сообщения следуют шаблону для событий DirectShow, а не Media Foundation событий.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**имфклокк**](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | Представляет часы Евр. Выступающий использует этот интерфейс для планирования образцов для представления. Евр может выполняться без часов, поэтому этот интерфейс может быть недоступен. В противном случае не обращайте внимания на код ошибки из [**лукупсервице**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).<br/> Часы также реализуют интерфейс [**имфтимер**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) . В конвейере Media Foundation часы реализуют интерфейс [**имфпресентатионклокк**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) . Он не реализует этот интерфейс в DirectShow.<br/> |



 

Получите следующие интерфейсы из микшера:



| Интерфейс микшера                              | Описание                                                |
|----------------------------------------------|------------------------------------------------------------|
| [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | Позволяет выступающим взаимодействовать с микшером.       |
| [**имфвидеодевицеид**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | Позволяет выступающему проверить GUID устройства микшера. |



 

Следующий код реализует метод [**инитсервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Если указатели интерфейса, полученные из [**лукупсервице**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) , больше не являются допустимыми, ЕВР вызывает [**Имфтопологисервицелукупклиент:: релеасесервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers). В этом методе Освободите все указатели интерфейсов и задайте для параметра Состояние выступающего значение Завершение работы:


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



Евр вызывает [**релеасесервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) по различным причинам, включая:

-   Отключение или повторное соединение ПИН-кодов (DirectShow), добавление или удаление приемников потоков (Media Foundation).
-   Изменение формата.
-   Установка новых часов.
-   Окончательное завершение работы Евр.

В течение времени жизни выступающего Евр может вызывать [**инитсервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) и [**релеасесервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) несколько раз.

### <a name="implementing-imfvideopresenter"></a>Реализация Имфвидеопресентер

Интерфейс [**имфвидеопресентер**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) наследует [**имфклоккстатесинк**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) и добавляет два метода:



| Метод                                                               | Описание                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [**жеткуррентмедиатипе**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | Возвращает тип мультимедиа для кадров составного видео. |
| [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | Сигнализирует ведущему выполнять различные действия.      |



 

Метод [**жеткуррентмедиатипе**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) Возвращает тип мультимедиа выступающего. (Дополнительные сведения о настройке типа мультимедиа см. в разделе [Форматирование согласования](#negotiating-formats).) Тип носителя возвращается как указатель интерфейса [**имфвидеомедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) . В следующем примере предполагается, что выступающий хранит тип мультимедиа как указатель [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Чтобы получить интерфейс **имфвидеомедиатипе** из типа мультимедиа, вызовите метод **QueryInterface**:


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Метод [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) является основным механизмом для Евр взаимодействия с выступающим. Определены следующие сообщения. Сведения о реализации каждого сообщения приведены в оставшейся части этого раздела.



| Сообщение                                | Описание                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVP_MESSAGE_INVALIDATEMEDIATYPE** | Недопустимый тип выходного носителя микшера. Выступающий должен согласовать новый тип мультимедиа с микшером. См. раздел [форматы согласования](#negotiating-formats).                                                                                         |
| **MFVP_MESSAGE_BEGINSTREAMING**      | Потоковая передача начата. Это сообщение не требует определенных действий, но его можно использовать для выделения ресурсов.                                                                                                                                 |
| **MFVP_MESSAGE_ENDSTREAMING**        | Потоковая передача завершена. Освободите все ресурсы, выделенные в ответ на **MFVP_MESSAGE_BEGINSTREAMING** сообщение.                                                                                                                        |
| **MFVP_MESSAGE_PROCESSINPUTNOTIFY**  | Микшер получил новый входной пример и может создать новый выходной фрейм. Выступающий должен вызвать [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) в микшере. См. раздел [Обработка выходных данных](#processing-output). |
| **MFVP_MESSAGE_ENDOFSTREAM**         | Презентация завершена. См. [конец потока](#end-of-stream).                                                                                                                                                                                   |
| **MFVP_MESSAGE_FLUSH**               | Евр очищает данные в конвейере отрисовки. Выступающий должен отбросить все кадры видео, запланированные для презентации.                                                                                                         |
| **MFVP_MESSAGE_STEP**                | Запрашивает у выступающего на шаг вперед N кадров. Выступающий должен отбросить следующие N-1 кадра и отобразить значение n. См. раздел [пошаговое выполнение](#frame-stepping).                                                                                |
| **MFVP_MESSAGE_CANCELSTEP**          | Отмена пошагового выполнения кадра.                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a>Реализация Имфклоккстатесинк

Выступающий должен реализовать интерфейс [**имфклоккстатесинк**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) как часть своей реализации [**имфвидеопресентер**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), которая наследует **имфклоккстатесинк**. Евр использует этот интерфейс для уведомления выступающего при каждом изменении состояния часов Евр. Дополнительные сведения о состояниях часов см. в статье [часы представления](presentation-clock.md).

Ниже приведены некоторые рекомендации по реализации методов в этом интерфейсе. При завершении работы Presenter все методы должны завершаться ошибкой.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>онклоккстарт</strong></a></td>
<td><ol>
<li>Установите состояние выступающего в значение Started.</li>
<li>Если <em>ллклоккстартоффсет</em> не <strong>PRESENTATION_CURRENT_POSITION</strong>, очистите очередь выступающих образцов. (Это эквивалентно получению сообщения <strong>MFVP_MESSAGE_FLUSH</strong> .)</li>
<li>Если предыдущий запрос шага кадра все еще находится в состоянии ожидания, обработайте запрос (см. раздел <a href="#frame-stepping">пошаговое выполнение</a>). В противном случае попробуйте обработать выходные данные микшера (см. раздел <a href="#processing-output">Обработка выходных данных</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>онклоккстоп</strong></a></td>
<td><ol>
<li>Установите состояние выступающего в значение Stopped.</li>
<li>Очистка очереди выступающих образцов.</li>
<li>Отмените все ожидающие операции в кадрах.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>онклоккпаусе</strong></a></td>
<td>Установка состояния выступающего в состояние "приостановлено".</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>онклоккрестарт</strong></a></td>
<td>Обрабатываются так же, как <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>онклоккстарт</strong></a> , но не удаляют очередь образцов.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>онклокксетрате</strong></a></td>
<td><ol>
<li>Если скорость меняется с нуля на ненулевой, отмените пошаговое выполнение кадра.</li>
<li>Хранить новую ставку часов. Частота представления зависят от часов. Дополнительные сведения см. в разделе <a href="#scheduling-samples">примеры планирования</a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a>Реализация Имфратесуппорт

Чтобы обеспечить поддержку скорости воспроизведения, отличной от скорости 1 ×, выступающий должен реализовать интерфейс [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) . Ниже приведены некоторые рекомендации по реализации методов в этом интерфейсе. После завершения работы Presenter все методы должны завершаться ошибкой. Дополнительные сведения об этом интерфейсе см. в разделе [Rate Control](rate-control.md).



| Значение                                                          | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жетсловестрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | Возвращает ноль, чтобы не указывать минимальную скорость воспроизведения.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**жетфастестрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | При нетонком воспроизведении скорость воспроизведения не должна превышать частоту обновления монитора: *Максимальная* частота  =  *обновления* (Гц)/ *Частота кадров видео* (кадров/с). Частота кадров видео указывается в типе носителя выступающего. <br/> Для тонкого воспроизведения скорость воспроизведения не ограничена; возвращайте значение **FLT_MAX**. На практике источник и декодер будут ограничивающими факторами при тонком воспроизведении. <br/> Для обратного воспроизведения возвратите отрицательное значение максимальной скорости.<br/> |
| [**исратесуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | Возвращает **MF_E_UNSUPPORTED_RATE** , если абсолютное значение *флрате* превышает максимальную скорость воспроизведения в выступающем. Вычислите максимальную скорость воспроизведения, как описано в [**жетфастестрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).                                                                                                                                                                                                                                                                                    |



 

В следующем примере показано, как реализовать метод [**жетфастестрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) :


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



В предыдущем примере вызывается вспомогательный метод Жетмаксрате для вычисления максимальной скорости прямого воспроизведения:

В следующем примере показано, как реализовать метод [**исратесуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) :


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a>Отправка событий в Евр

Выступающий должен уведомлять Евр различных событий. Для этого используется интерфейс [**ИМЕДИАЕВЕНТСИНК**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) евр, полученный, когда Евр вызывает метод [**Имфтопологисервицелукупклиент:: инитсервицепоинтерс**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) выступающего. (Интерфейс **имедиаевентсинк** изначально является интерфейсом DirectShow, но используется как в Евр DirectShow, так и в Media Foundation.) В следующем коде показано, как отправить событие в Евр:


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



В следующей таблице перечислены события, отправляемые выступающим, а также параметры событий.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Событие</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></td>
<td>Выступающий завершил отрисовку всех кадров после сообщения MFVP_MESSAGE_ENDOFSTREAM.<br/>
<ul>
<li><em>Param1</em>: HRESULT, указывающий состояние операции.</li>
<li><em>Param2</em>: не используется.</li>
</ul>
Дополнительные сведения см. в разделе <a href="#end-of-stream">конец потока</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></td>
<td>Устройство Direct3D изменилось.<br/>
<ul>
<li><em>Param1</em>: не используется.</li>
<li><em>Param2</em>: не используется.</li>
</ul>
Дополнительные сведения см. <a href="#managing-the-direct3d-device">в разделе Управление устройством Direct3D</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></td>
<td>Произошла ошибка, для которой требуется остановленная потоковая передача.<br/>
<ul>
<li><em>Param1</em>: <strong>HRESULT</strong> , указывающий возникшую ошибку.</li>
<li><em>Param2</em>: не используется.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></td>
<td>Указывает время, в течение которого выступающий готовится к просмотру каждого кадра. (Необязательно.)<br/>
<ul>
<li><em>Param1</em>: указатель на константное значение <strong>лонглонг</strong> , которое содержит количество времени для обработки кадра в единицах измерения 100-наносекундных.</li>
<li><em>Param2</em>: не используется.</li>
</ul>
Дополнительные сведения см. в разделе <a href="#processing-output">Обработка выходных данных</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></td>
<td>Указывает текущее время запаздывания в примерах отрисовки. Если значение положительное, выборка отстает от расписания. Если значение отрицательное, выборки выполняются заранее по расписанию. (Необязательно.)<br/>
<ul>
<li><em>Param1</em>: указатель на константное значение <strong>лонглонг</strong> , которое содержит время запаздывания в единицах измерения 100-наносекундных.</li>
<li><em>Param2</em>: не используется.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></td>
<td>Отправляется сразу после <strong>EC_STEP_COMPLETE</strong> , если скорость воспроизведения равна нулю. Это событие содержит метку времени отображаемого кадра.<br/>
<ul>
<li><em>Param1</em>: младшие 32 бит метки времени.</li>
<li><em>Param2</em>: верхний 32 бит метки времени.</li>
</ul>
Дополнительные сведения см. в разделе <a href="#frame-stepping">пошаговая отладка кадров</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></td>
<td>Выступающий завершил или отменил шаг кадра.<br/>
<ul>
<li><em>Param1</em>: не используется.</li>
<li><em>Param2</em>: не используется.</li>
</ul>
Дополнительные сведения см. в разделе <a href="#frame-stepping">пошаговая отладка кадров</a>.<br/>
<blockquote>
[!Note]<br />
Предыдущая версия документации неправильно описывала параметр <em>param1</em> . Этот параметр не используется для этого события.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a>Форматы согласования

Всякий раз, когда выступающий получает сообщение **MFVP_MESSAGE_INVALIDATEMEDIATYPE** из евр, оно должно задать выходной формат для микшера следующим образом:

1.  Вызовите [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) в микшере, чтобы получить возможный тип выходных данных. Этот тип описывает формат, который микшер может создать при наличии входных потоков и возможностей обработки видео графического устройства.
2.  Проверьте, может ли выступающий использовать этот тип мультимедиа в качестве формата подготовки к просмотру. Ниже приведены некоторые вещи, которые необходимо проверить, хотя реализация может иметь собственные требования.

    -   Видео должно быть распаковано.
    -   В видео должны быть только прогрессивные кадры. Убедитесь, что атрибут [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) равен **MFVideoInterlace_Progressive**.
    -   Формат должен быть совместим с устройством Direct3D.

    Если тип неприемлем, вернитесь к шагу 1 и получите следующий предложенный тип микшера.

3.  Создайте новый тип мультимедиа, который является клоном исходного типа, а затем измените следующие атрибуты:

    -   Присвойте атрибуту [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) значение, равное ширине и высоте, которые будут выделяться для поверхностей Direct3D.
    -   Присвойте [](mf-mt-pan-scan-enabled-attribute.md) атрибуту MF_MT_PAN_SCAN_ENABLED **значение false**.
    -   Установите атрибут [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) РАВНым номиналу дисплея (обычно 1:1).
    -   Установите геометрическое апертуру ([**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) атрибут) равным прямоугольнику в области Direct3D. Когда микшер создает выходной кадр, он блитс исходный образ на этот прямоугольник. Геометрическое Апертура может быть большим, чем поверхность, или подпрямоугольником внутри области. Дополнительные сведения см. в разделе [прямоугольники источника и назначения](#source-and-destination-rectangles).

4.  Чтобы проверить, примет ли микшер измененный тип вывода, вызовите [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) с флагом **MFT_SET_TYPE_TEST_ONLY** . Если микшер отклоняет тип, вернитесь к шагу 1 и получите следующий тип.
5.  Выделите пул поверхностей Direct3D, как описано в разделе [выделение поверхностей Direct3D](#allocating-direct3d-surfaces). Микшер будет использовать эти поверхности при рисовании составных кадров видео.
6.  Задайте тип выходных данных микшера, вызвав [**сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) без флагов. Если в шаге 4 первый вызов **сетаутпуттипе** завершился удачно, метод должен пройти повторно.

Если микшер выполняется из типов, метод [**жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) возвращает **MF_E_NO_MORE_TYPES**. Если выступающий не может найти подходящий тип выходных данных для микшера, поток не может быть визуализирован. В этом случае DirectShow или Media Foundation могут использовать другой формат потока. Таким образом, выступающий может получить несколько **MFVP_MESSAGE_INVALIDATEMEDIATYPE** сообщений в строке, пока не будет найден допустимый тип.

Микшер автоматически леттербоксес видео, принимая во внимание пропорцию пикселя (номинал) источника и назначения. Для достижения лучших результатов ширина и высота поверхности и геометрический апертуры должны быть равны фактическому размеру, который должен отображаться на экране. Этот процесс показан на следующем рисунке.

![Схема, демонстрирующая составной Фрам, ведущей к поверхности Direct3D, которая ведет к окну](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

В следующем коде показана структура процесса. Некоторые шаги помещаются в вспомогательные функции, подробные сведения о которых будут зависеть от требований вашего Presenter.


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



Дополнительные сведения о типах мультимедиа см. в статье [типы видеороликов](video-media-types.md).

## <a name="managing-the-direct3d-device"></a>Управление устройством Direct3D

Выступающий создает устройство Direct3D и обрабатывает потери устройств во время потоковой передачи. В выступающих также размещается Диспетчер устройств Direct3D, который предоставляет другим компонентам возможность использовать одно и то же устройство. Например, микшер использует устройство Direct3D для смешивания подпотоков, дечередования и настройки цветов. Декодеры могут использовать устройство Direct3D для декодирования с помощью ускорения видео. (Дополнительные сведения об ускорении видео см. в статье [DirectX Video ускорение 2,0](directx-video-acceleration-2-0.md).)

Чтобы настроить устройство Direct3D, выполните следующие действия.

1.  Создайте объект Direct3D, вызвав **Direct3DCreate9** или **Direct3DCreate9Ex**.
2.  Создайте устройство, вызвав **IDirect3D9:: креатедевице** или **IDirect3D9Ex:: креатедевице**.
3.  Создайте диспетчер устройств, вызвав [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).
4.  Настройте устройство в диспетчере устройств, вызвав [**IDirect3DDeviceManager9:: ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).

Если другому компоненту конвейера требуется диспетчер устройств, он вызывает [**имфжетсервице::**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Евр в, указывая **MR_VIDEO_ACCELERATION_SERVICE** для идентификатора GUID службы. Евр передает запрос выступающему. После того как объект получает указатель [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) , он может получить маркер устройства, вызвав [**IDirect3DDeviceManager9:: опендевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle). Когда объекту требуется использовать устройство, он передает его методу [**IDirect3DDeviceManager9:: локкдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) , который возвращает указатель **IDirect3DDevice9** .

Если после создания устройства выступающий уничтожает устройство и создает новый, он должен вызвать [**ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) еще раз. Метод **ресетдевице** делает недействительными все существующие дескрипторы устройств, что приводит к возвращению [**локкдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) **DXVA2_E_NEW_VIDEO_DEVICE**. Этот код ошибки сигнализирует другим объектам с помощью устройства, что им следует открыть новый обработчик устройства. Дополнительные сведения об использовании диспетчера устройств см. в разделе [Direct3D Диспетчер устройств](direct3d-device-manager.md).

Выступающий может создать устройство в оконном режиме или в полноэкранном режиме монопольного доступа. Для оконного режима следует предоставить приложению способ указания окна видео. Стандартный выступающий реализует метод [**имфвидеодисплайконтрол:: сетвидеовиндов**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) для этой цели. Необходимо создать устройство при первом создании Presenter. Как правило, в настоящее время вы не узнаете все параметры устройства, например окно или формат заднего буфера. Вы можете создать временное устройство и заменить его позже&\# . просто не забудьте вызвать [**ресетдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) в диспетчере устройств.

Если вы создаете новое устройство или вызываете **IDirect3DDevice9:: Reset** или **IDirect3DDevice9Ex:: ресетекс** на существующем устройстве, отправьте событие [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) в Евр. Это событие уведомляет Евр о необходимости повторного согласования типа носителя. Евр игнорирует параметры события для этого события.

### <a name="allocating-direct3d-surfaces"></a>Выделение поверхностей Direct3D

После того как выступающий задает тип мультимедиа, он может выделить поверхности Direct3D, которые микшер будет использовать для записи кадров видео. Поверхность должна соответствовать типу мультимедиа выступающего:

-   Формат поверхности должен соответствовать подтипу носителя. Например, если подтип имеет значение **MFVideoFormat_RGB24**, формат поверхности должен быть **D3DFMT_X8R8G8B8**. Дополнительные сведения о подтипах и форматах Direct3D см. в разделе [GUID подтипов видео](video-subtype-guids.md).
-   Ширина и высота поверхности должны соответствовать измерениям, заданным в атрибуте [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) типа мультимедиа.

Рекомендуемый способ распределения поверхностей зависит от того, выполняется ли в окне полноэкранный режим.

Если устройство Direct3D является оконным, можно создать несколько цепочек подкачки, каждый из которых имеет один задний буфер. Используя этот подход, можно отдельно представлять каждую поверхность, так как представление одной цепочки подкачки не мешает другим цепочкам подкачки. Микшер может записывать данные на поверхность, в то время как на другую поверхность планируется презентация.

Сначала определите, сколько цепочек подкачки следует создать. Рекомендуется как минимум три. Для каждой цепочки подкачки выполните следующие действия.

1.  Вызовите метод **IDirect3DDevice9:: креатеаддитионалсвапчаин** , чтобы создать цепочку буферов.
2.  Вызовите **IDirect3DSwapChain9:: жетбаккбуффер** , чтобы получить указатель на поверхность буфера обратной цепочки.
3.  Вызовите [**мфкреатевидеосамплефромсурфаце**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) и передайте указатель на поверхность. Эта функция возвращает указатель на видеообъект образца видео. Пример объекта Video реализует интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , и он использует этот интерфейс для передачи поверхности в микшер, когда выступающий вызывает метод микшера [**Имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Дополнительные сведения об объекте видео Sample см. в разделе [образцы видео](video-samples.md).
4.  Сохранение указателя [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) в очереди. Выступающие выводит примеры из этой очереди во время обработки, как описано в разделе [Обработка выходных данных](#processing-output).
5.  Сохраняет ссылку на указатель **IDirect3DSwapChain9** , чтобы цепочка буферов не была освобождена.

В полноэкранном монопольном режиме устройство не может иметь более одной цепочки буферов. Эта цепочка буфера обмена создается неявно при создании полноэкранного устройства. Цепочка буферов может иметь более одного заднего буфера. К сожалению, тем не менее, если вы предоставляете один задний буфер во время записи в другой задний буфер в той же цепочке буферов, нет простого способа координировать две операции. Это обусловлено тем, как Direct3D реализует перелистывание поверхностей. При вызове Present драйвер графики обновляет указатели поверхности в графической памяти. Если при вызове **присутствовали** указатели **IDirect3DSurface9** , они будут указывать на различные буферы после возврата **текущего** вызова.

Самый простой вариант — создать один видеопример для цепочки буферов. Если выбран этот параметр, выполните те же действия, что и для оконного режима. Единственное отличие состоит в том, что пример очереди содержит один пример видео. Другой вариант — создать поверхностные поверхности, а затем Блит их в задний буфер. Создаваемые поверхности должны поддерживать метод [**идиректксвидеопроцессор:: видеопроцессблт**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) , который микшер использует для совмещения выходных кадров.

### <a name="tracking-samples"></a>Примеры. Отслеживание

Когда выступающий сначала выделяет образцы видео, он помещает их в очередь. Выступающий рисует из этой очереди каждый раз, когда ему нужно получить новый кадр из микшера. Когда микшер выводит кадр, он перемещает пример во вторую очередь. Вторая очередь предназначена для выборок, ожидающих времени показа по расписанию.

Чтобы упростить отслеживание состояния каждого образца, объект видео Sample реализует интерфейс [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) . Этот интерфейс можно использовать следующим образом:

1.  Реализуйте интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) в вашем выступающем.
2.  Перед тем как поместить пример в очередь по расписанию, запросите объект видео Sample для интерфейса [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .

3.  Вызовите [**имфтраккедсампле:: сеталлокатор**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) с указателем на интерфейс обратного вызова.
4.  Когда образец готов к показу, удалите его из очереди запланированных, приготовьте его и освободите все ссылки на этот пример.
5.  В примере вызывается обратный вызов. (Образец объекта в этом случае не удаляется, так как он содержит счетчик ссылок на себя до вызова обратного вызова.)
6.  В обратном вызове верните пример в доступную очередь.

Выступающий не требуется использовать [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) для наблюдения за примерами; можно реализовать любой метод, который лучше подходит для вашего проекта. Одно из преимуществ **имфтраккедсампле** заключается в том, что функции планирования и подготовки выступающего можно переместить в вспомогательные объекты, и для этих объектов не требуется специальный механизм для обратного вызова к выступающему, когда они выпускают образцы видео, так как пример объекта предоставляет этот механизм.

В следующем коде показано, как задать обратный вызов:


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



В обратном вызове вызовите [**имфасинкресулт:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) в объекте асинхронного результата, чтобы получить указатель на образец:


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock ***/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /*** End lock ***/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a>Обработка выходных данных

Каждый раз, когда микшер получает новый входной пример, ЕВР отправляет выступающее сообщение **MFVP_MESSAGE_PROCESSINPUTNOTIFY** . Это сообщение означает, что микшер может иметь новый кадр видео для доставки. В ответ выступающий вызывает [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) в микшере. Если метод будет выполнен, выступающий планирует пример для презентации.

Чтобы получить выходные данные микшера, выполните следующие действия.

1.  Проверьте состояние часов. Если часы приостановлены, пропустите **MFVP_MESSAGE_PROCESSINPUTNOTIFY** сообщение, если это не первый кадр видео. Если часы выполняются или если это первый кадр видео, продолжайте.
2.  Получите пример из очереди доступных образцов. Если очередь пуста, это означает, что все выделенные образцы в настоящее время запланированы для показа. В этом случае проигнорируйте сообщение **MFVP_MESSAGE_PROCESSINPUTNOTIFY** в данный момент. Когда следующий образец станет доступным, повторите приведенные здесь действия.
3.  (Необязательно.) Если часы доступны, получите текущее время (*T1*), вызвав [**Имфклокк:: жеткоррелатедтиме**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).
4.  Вызовите [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) в микшере. Если **ProcessOutput** выполнена, пример содержит видеокадр. Если метод завершается ошибкой, проверьте код возврата. Следующие коды ошибок от **ProcessOutput** не являются критическими сбоями:

    

    | Код ошибки                              | Описание                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **MF_E_TRANSFORM_NEED_MORE_INPUT** | Перед созданием нового выходного фрейма для микшера требуется больше входных данных.<br/> Если вы получаете этот код ошибки, проверьте, достиг ли Евр конца потока и отвечайте соответствующим образом, как описано в [конце потока](#end-of-stream). В противном случае пропустите это **MF_E_TRANSFORM_NEED_MORE_INPUT** сообщение. Евр отправит еще один, когда микшер получит больше входных данных.<br/> |
    | **MF_E_TRANSFORM_STREAM_CHANGE**    | Тип выходных данных микшера стал недопустимым, возможно, из-за изменения формата.<br/> Если вы получаете этот код ошибки, установите для типа мультимедиа в качестве носителя **значение NULL**. Евр будет запрашивать новый формат.<br/>                                                                                                                                                                         |
    | **MF_E_TRANSFORM_TYPE_NOT_SET**    | Для микшера требуется новый тип носителя.<br/> Если вы получаете этот код ошибки, повторно согласовывайте тип вывода микшера, как описано в разделе [форматы согласования](#negotiating-formats).<br/>                                                                                                                                                                                                        |

    

     

    Если [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) будет выполнена, продолжайте.

5.  (Необязательно.) Если часы доступны, получите текущее время (*T2*). Количество задержек, введенных микшером, — (*T2*  -  *T1*). Отправка **EC_PROCESSING_LATENCY** события с этим ЗНАЧЕНИЕМ в Евр. Евр использует это значение для контроля качества. Если часы недоступны, нет причин отправить событие **EC_PROCESSING_LATENCY** .
6.  (Необязательно.) Выполните запрос к образцу для [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) и вызовите [**Имфтраккедсампле:: сеталлокатор**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) , как описано в разделе о [примерах отслеживания](#tracking-samples).
7.  Запланируйте пример для презентации.

Эта последовательность действий может завершиться до того, как выступающий получит выходные данные микшера. Чтобы предотвратить удаление запросов, необходимо повторить те же действия, что и в следующем случае.

-   Вызывается метод [**имфклоккстатесинк:: онклоккстарт**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) или **Имфклоккстатесинк:: онклоккстарт** выступающего. Это обрабатывает случай, когда микшер игнорирует входные данные, так как часы приостанавливаются (шаг 1).
-   Вызывается обратный вызов [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) . Это обрабатывает случай, когда микшер получает входные данные, но все видеоматериалы в выступающем коде используются (шаг 2).

В следующих нескольких примерах кода эти действия показаны более подробно. Выступающий вызывает `ProcessInputNotify` метод (как показано в следующем примере), когда он получает сообщение **MFVP_MESSAGE_PROCESSINPUTNOTIFY** .


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



Этот `ProcessInputNotify` метод задает логический флаг для записи того факта, что микшер имеет новые входные данные. Затем вызывается `ProcessOutputLoop` метод, показанный в следующем примере. Этот метод пытается извлечь из микшера столько выборок, сколько возможно:


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



`ProcessOutput`Метод, показанный в следующем примере, пытается получить один кадр видео из микшера. Если видеокадр недоступен, `ProcessSample` возвращает S_FALSE или код ошибки, который прерывает цикл в `ProcessOutputLoop` . Большая часть работы выполняется внутри `ProcessOutput` метода:


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



Некоторые замечания по этому примеру:

-   Предполагается, что *m_SamplePool* переменная является объектом коллекции, в котором хранится очередь доступных видеороликов. `GetSample`Метод объекта возвращает **MF_E_SAMPLEALLOCATOR_EMPTY** , если очередь пуста.
-   Если метод [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) микшера возвращает MF_E_TRANSFORM_NEED_MORE_INPUT, это означает, что микшер не может получить больше выходных данных, так что выступающий снимает флаг *m_fSampleNotify* .
-   `TrackSample`Метод, который задает обратный вызов [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) , показан в разделе [примеры отслеживания](#tracking-samples).

### <a name="repainting-frames"></a>Перерисовка кадров

Иногда выступающим может потребоваться перекрасить последний кадр видео. Например, Стандартный выступающий перерисовывает кадр в следующих ситуациях:

-   В оконном режиме, в ответ на **WM_PAINT** сообщения, полученные окном приложения. См. раздел [**имфвидеодисплайконтрол:: репаинтвидео**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).
-   Значение, если конечный прямоугольник изменяется, когда приложение вызывает [**имфвидеодисплайконтрол:: сетвидеопоситион**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Выполните следующие действия, чтобы запросить микшер для повторного создания последней рамки:

1.  Получите пример видео из очереди.
2.  Запросите пример для интерфейса [**имфдесиредсампле**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) .
3.  Вызовите [**имфдесиредсампле:: сетдесиредсамплетимеанддуратион**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration). Укажите метку времени для последнего кадра видео. (Вам потребуется кэшировать это значение и обновить его для каждого кадра.)
4.  Вызовите [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) в микшере.

При перерисовки рамки можно проигнорировать часы презентации и сразу приступить к показу кадра.

### <a name="scheduling-samples"></a>Примеры планирования

Видеокадры могут достигать Евр в любое время. Выступающий отвечает за представление каждого кадра в нужное время на основе метки времени кадра. Когда выступающий получает новый пример из микшера, он помещает пример в очередь по расписанию. В отдельном потоке, выступающий постоянно получает первый пример из заголовка очереди и определяет, нужно ли:

-   Представьте пример.
-   Не заключайте пример в очередь, так как он находится на раннем этапе.
-   Удалите пример, так как он просрочен. Несмотря на то, что по возможности не следует удалять кадры, может потребоваться, если выступающие непрерывно не попадают.

Чтобы получить метку времени для видеокадра, вызовите [**имфсампле:: жетсамплетиме**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) в примере с видео. Метка времени относится к часам представления Евр. Чтобы получить текущее время, вызовите метод [**имфклокк:: жеткоррелатедтиме**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime). Если Евр не имеет часов представления или если образец не имеет отметки времени, вы можете предоставить пример сразу же после его получения.

Чтобы получить длительность каждого образца, вызовите метод [**имфсампле:: жетсампледуратион**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration). Если выборка не имеет длительности, можно использовать функцию [**мффрамератетоаверажетимеперфраме**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) для вычисления длительности по частоте кадров.

При планировании выборок учитывайте следующее.

-   Если скорость воспроизведения увеличивается или снижается по сравнению с обычной скоростью, часы запускаются с более высокой или низкой скоростью. Это означает, что метка времени в образце всегда дает правильное целевое время относительно часов представления. Однако при переводе времени презентации в другое время (например, счетчик производительности с высоким разрешением) необходимо масштабировать время в зависимости от тактовой частоты. При изменении тактовой частоты Евр вызывает метод [**имфклоккстатесинк:: онклокксетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) выступающего.
-   Скорость воспроизведения может быть отрицательной для воспроизведения на противоположном. Если скорость воспроизведения отрицательна, часы презентации выполняются назад. Иными словами, время *n* + 1 происходит раньше, чем время *n*.

В следующем примере вычисляется, как на ранней или поздней стадии выполняется выборка относительно часов представления.


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



Часы презентации обычно управляются системными часами или модулем подготовки звука. (Модуль подготовки звука наследует время от скорости, с которой звуковая карта потребляет звук.) Как правило, часы представления не синхронизируются с частотой обновления монитора.

Если параметры представления Direct3D указывают **D3DPRESENT_INTERVAL_DEFAULT** или **D3DPRESENT_INTERVAL_ONE** для интервала презентации, операция **представления** ожидает вертикальной перетрассировки монитора. Это простой способ предотвратить разрыв, но снижает точность алгоритма планирования. И наоборот, если интервал презентации **D3DPRESENT_INTERVAL_IMMEDIATE**, то метод **Present** выполняется немедленно, что приводит к разрыву, если только алгоритм планирования не будет достаточно точным, пока вы не назначите **его только в** течение вертикального периода повторной трассировки.

Следующие функции помогут получить точные сведения о времени:

-   **IDirect3DDevice9:: жетрастерстатус** возвращает сведения о растровом элементе, включая текущую строку развертки, а также то, находится ли точечный символ в вертикальной пустой точке.
-   **Двмжеткомпоситионтимингинфо** возвращает сведения о времени для диспетчера окон рабочего стола. Эта информация полезна, если включена Композиция рабочего стола.

### <a name="presenting-samples"></a>Представление образцов

В этом разделе предполагается, что вы создали отдельную цепочку подкачки для каждой поверхности, как описано в статье [выделение поверхностей Direct3D](#allocating-direct3d-surfaces). Чтобы показать пример, получите цепочку подкачки из примера видео следующим образом:

1.  Чтобы получить буфер, вызовите [**имфсампле:: жетбуффербиндекс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) в примере видео.
2.  Запросите буфер для интерфейса [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
3.  Вызовите [**имфжетсервице:: Get Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , чтобы получить интерфейс **IDirect3DSurface9** поверхности Direct3D. (Этот шаг и предыдущий шаг можно объединить в один, вызвав [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)
4.  Вызовите **IDirect3DSurface9::-Contain** на поверхности, чтобы получить указатель на цепочку буферов.
5.  Вызов **IDirect3DSwapChain9::P** повторной отправки в цепочке буферов.

Следующий код показывает эти действия.


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a>Исходный и конечный прямоугольники

*Исходный прямоугольник* — это часть отображаемого видеокадра. Он определяется относительно нормализованной системы координат, в которой весь кадр видео занимает прямоугольник с координатами {0, 0, 1, 1}. *Прямоугольник назначения* — это область в области назначения, в которой рисуется кадр видео. Стандартный выступающий позволяет приложению устанавливать эти прямоугольники путем вызова [**имфвидеодисплайконтрол:: сетвидеопоситион**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Существует несколько вариантов применения исходного и целевого прямоугольников. Первый вариант — Разрешить микшеру применять их:

-   Задайте исходный прямоугольник с помощью атрибута [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) . Микшер будет применять исходный прямоугольник, когда он блитс видео на поверхность назначения. Исходный прямоугольник по умолчанию — это весь фрейм.
-   Установите прямоугольник назначения в качестве геометрического апертуры в выходном типе микшера. Дополнительные сведения см. в статье о [форматах согласования](#negotiating-formats).

Второй вариант — применить прямоугольники при **IDirect3DSwapChain9::P** повторно, указав параметры *псаурцерект* и *пдестрект* в методе **Present** . Эти параметры можно комбинировать. Например, можно задать исходный прямоугольник в микшере, но применить прямоугольник назначения в методе **Present** .

Если приложение изменяет конечный прямоугольник или изменяет размер окна, может потребоваться выделить новые поверхности. Если это так, необходимо соблюдать осторожность при синхронизации этой операции с потоком планирования. Очистите очередь планирования и отбросить старые примеры перед выделением новых поверхностей.

### <a name="end-of-stream"></a>Конец потока

После завершения каждого входного потока в Евр Евр отправляет выступающее сообщение **MFVP_MESSAGE_ENDOFSTREAM** . Однако в момент получения сообщения может быть осталось несколько кадров видео, которые будут обработаны. Прежде чем реагировать на сообщение в конце потока, необходимо прекратить все выходные данные микшера и Показать все остальные кадры. После представления последнего кадра Отправьте событие **EC_COMPLETE** в Евр.

В следующем примере показан метод, который отправляет событие **EC_COMPLETE** , если выполняются различные условия. В противном случае он возвращает S_OK без отправки события:


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



Этот метод проверяет следующие состояния:

-   Если переменная *m_fSampleNotify* имеет **значение true**, это означает, что микшер содержит один или несколько кадров, которые еще не были обработаны. (Дополнительные сведения см. в разделе [Обработка выходных данных](#processing-output).)
-   Переменная *m_fEndStreaming* является логическим флагом, начальным значением которого является **false**. Выступающий устанавливает для флага **значение true** , когда Евр отправляет сообщение **MFVP_MESSAGE_ENDOFSTREAM** .
-   `AreSamplesPending`Предполагается, что метод возвращает **значение true** , если один или несколько кадров ожидают выполнения в запланированной очереди.

В методе [**имфвидеопресентер::P роцессмессаже**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) задайте для *m_fEndStreaming* **значение true** и вызовите, `CheckEndOfStream` когда Евр отправляет сообщение **MFVP_MESSAGE_ENDOFSTREAM** :


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Кроме того, вызовите, `CheckEndOfStream` Если метод [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) микшера возвращает **MF_E_TRANSFORM_NEED_MORE_INPUT**. Этот код ошибки означает, что микшер не содержит дополнительных входных образцов (см. раздел [Обработка выходных данных](#processing-output)).

## <a name="frame-stepping"></a>Пошаговое выполнение кадра

Евр предназначен для поддержки пошагового выполнения кадров в DirectShow и очистки в Media Foundation. Пошаговое выполнение и очистка кадров концептуально похожи. В обоих случаях приложение запрашивает один видеокадр за раз. На внутреннем уровне выступающий использует тот же механизм для реализации обеих функций.

Пошаговое выполнение пакета в DirectShow работает следующим образом:

-   Приложение вызывает [**ивидеофраместеп:: Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step). Число шагов указывается в параметре *двстепс* . Евр отправляет выступающее сообщение **MFVP_MESSAGE_STEP** , где параметр сообщения (*улпарам*) — это число шагов.
-   Если приложение вызывает [**ивидеофраместеп:: канцелстеп**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) или изменяет состояние графа (запущено, приостановлено или остановлено), ЕВР отправляет сообщение **MFVP_MESSAGE_CANCELSTEP** .

Очистка в Media Foundation работает следующим образом:

-   Приложение устанавливает скорость воспроизведения равным нулю, вызывая [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).
-   Чтобы отобразить новый кадр, приложение вызывает [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) с требуемой позицией. Евр отправляет сообщение **MFVP_MESSAGE_STEP** с *улпарам* , равным 1.
-   Чтобы отключить очистку, приложение устанавливает для скорости воспроизведения ненулевое значение. Евр отправляет сообщение **MFVP_MESSAGE_CANCELSTEP** .

После получения сообщения **MFVP_MESSAGE_STEP** Выступающий ожидает прибытия целевого кадра. Если число шагов равно *N*, то выступающий отклоняет следующие примеры (*n* – 1) и представляет *N* -й пример. Когда выступающий завершает шаг кадра, он отправляет событие [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) в Евр с параметром *lParam1* , имеющим значение **false**. Кроме того, если скорость воспроизведения равна нулю, выступающий отправляет событие [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) . Если Евр отменяет выполнение кадра в то время, когда операция с кадрами все еще находится в состоянии ожидания, выступающий отправляет событие **EC_STEP_COMPLETE** с параметром *lParam1* , имеющим значение **true**.

Приложение может выполнить шаг или очистку несколько раз, поэтому перед получением **MFVP_MESSAGE_CANCELSTEP** сообщения выступающий может получить несколько **MFVP_MESSAGE_STEP** сообщений. Кроме того, выступающий может получить сообщение **MFVP_MESSAGE_STEP** до начала или во время выполнения часов.

### <a name="implementing-frame-stepping"></a>Реализация пошагового выполнения кадра

В этом разделе описывается алгоритм для реализации пошагового выполнения кадра. Алгоритм пошагового выполнения кадров использует следующие переменные:

-   *step_count*. Целое число без знака, указывающее количество шагов в текущей операции пошагового выполнения кадра.
-   *step_queue*. Очередь указателей [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .
-   *step_state*. В любое время выступающий может находиться в одном из следующих состояний по отношению к пошаговому выполнению кадров: 

    | Состояние         | Описание                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | NOT_STEPPING | Не пошаговое выполнение кадра.                                                                                                                                                                                             |
    | ОЖИДАНИЕ       | Выступающий получил сообщение **MFVP_MESSAGE_STEP** , но часы не запущены.                                                                                                                  |
    | PENDING       | Выступающий получил сообщение **MFVP_MESSAGE_STEP** , и часы начали, но выступающий ожидает получения целевого кадра.                                                             |
    | ПЛАНИРУЕТ     | Докладчик получил целевой кадр и запланировал его для презентации, но этот кадр не был представлен.                                                                                        |
    | ЗАВЕРШЕНИЯ      | Докладчик представил целевой кадр и отправил [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) событие и ожидает следующего сообщения **MFVP_MESSAGE_STEP** или **MFVP_MESSAGE_CANCELSTEP** . |

    

     

    Эти состояния не зависят от состояний выступающего, перечисленных в разделе [состояние Presenter](#presenter-states).

Для алгоритма пошагового прохода определены следующие процедуры:

Процедура Препарефраместеп

1.  *Step_count* приращения.
2.  Задайте для *step_state* значение ожидание.
3.  Если часы выполняются, вызовите Стартфраместеп.

Процедура Стартфраместеп

1.  Если *step_state* равно ожидания, присвойте *step_state* ожидания. Для каждого примера в *step_queue* вызовите деливерфраместепсампле.
2.  Если *step_state* равно NOT_STEPPING, удалите все образцы из *step_queue* и запланируйте их для представления.

Процедура Комплетефраместеп

1.  Задайте для *step_state* значение завершено.
2.  Отправьте событие EC_STEP_COMPLETE с *lParam1*  =  **false**.
3.  Если ставка часов равна нулю, отправьте событие **EC_SCRUB_TIME** с помощью образца Time.

Процедура Деливерфраместепсампле

1.  Если ставка часов равна нулю и время дискретизации выборки *времени*  +    <  , отбросить пример. Выйти.
2.  Если *step_state* равно "запланировано" или "завершено", добавьте пример в *step_queue*. Выйти.
3.  Декремента *step_count*.
4.  Если *step_count* > 0, удалите пример. Выйти.
5.  Если *step_state* равно ожидания, добавьте пример в *step_queue*. Выйти.
6.  Запланируйте пример для презентации.
7.  Задайте для *step_state* значение запланировано.

Процедура Канцелфраместеп

1.  Задайте для *step_state* значение NOT_STEPPING
2.  Сброс *step_count* к нулю.
3.  Если предыдущее значение *step_state* было ожидающим, ожидающим или запланированным, отправьте EC_STEP_COMPLETE с *lParam1*  =  **true**.

Вызовите эти процедуры следующим образом:



| Сообщение или метод выступающего                                                   | Процедура           |
|-------------------------------------------------------------------------------|---------------------|
| Сообщение **MFVP_MESSAGE_STEP**                                               | `PrepareFrameStep`  |
| Сообщение **MFVP_MESSAGE_STEP**                                               | `CancelStep`        |
| [**Имфклоккстатесинк:: Онклоккстарт**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [**Имфклоккстатесинк:: Онклоккрестарт**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| Обратный вызов [**имфтраккедсампле**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)                         | `CompleteFrameStep` |
| [**Имфклоккстатесинк:: Онклоккстоп**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [**Имфклоккстатесинк:: Онклокксетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

В следующей блок-схеме показаны процедуры пошагового выполнения.

![на блоковой диаграмме показаны пути, которые начинаются с \- шага сообщения мфвп \- и \- сообщения мфвп \- процессинпутнотифи и заканчиваются на "штат = Complete".](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a>Установка параметра Presenter в Евр

После реализации выступающего, следующим шагом является настройка Евр для его использования.

### <a name="setting-the-presenter-in-directshow"></a>Настройка выступающего в DirectShow

В приложении DirectShow установите параметр Presenter для Евр следующим образом:

1.  Создайте фильтр евр, вызвав **CoCreateInstance**. Идентификатор CLSID — **CLSID_EnhancedVideoRenderer**.
2.  Добавьте Евр в граф фильтра.
3.  Создайте экземпляр Presenter. Ваш выступающий может поддерживать создание стандартных объектов COM через **IClassFactory**, но это необязательно.
4.  Запросите фильтр Евр для интерфейса [**имфвидеорендерер**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .
5.  Вызовите [**имфвидеорендерер:: инитиализерендерер**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).

### <a name="setting-the-presenter-in-media-foundation"></a>Настройка выступающего в Media Foundation

В Media Foundation есть несколько вариантов в зависимости от того, создается ли приемник мультимедиа Евр или объект активации Евр. Дополнительные сведения об объектах активации см. в разделе [объекты активации](activation-objects.md).

Для приемника мультимедиа Евр выполните следующие действия.

1.  Вызовите [**мфкреатевидеорендерер**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) , чтобы создать приемник мультимедиа.
2.  Создайте экземпляр Presenter.
3.  Запросите приемник мультимедиа Евр для интерфейса [**имфвидеорендерер**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .
4.  Вызовите [**имфвидеорендерер:: инитиализерендерер**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).

Для объекта активации Евр выполните следующие действия.

1.  Вызовите [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) , чтобы создать объект активации.
2.  Задайте один из следующих атрибутов для объекта активации. 

    | attribute                                                                                                         | Описание                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Указатель на объект активации для выступающего объекта.<br/> При использовании этого флага необходимо предоставить объект активации для своего выступающего. Объект активации должен реализовывать интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .<br/> |
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | Идентификатор CLSID выступающего.<br/> Этот флаг должен поддерживать создание стандартного объекта COM с помощью **IClassFactory**.<br/>                                                                                         |

    

     

3.  При необходимости задайте атрибут [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) для объекта активации.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Улучшенный модуль подготовки видео](enhanced-video-renderer.md)
</dt> <dt>

[Пример Еврпресентер](evrpresenter-sample.md)
</dt> </dl>

 

 
