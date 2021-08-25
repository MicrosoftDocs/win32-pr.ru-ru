---
description: Режим без окон VMR
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Режим без окон VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193f672e0fc1e3dced4bdff16da0e85123079eb94f2ac3c5fdb302b67c9432b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830592"
---
# <a name="vmr-windowless-mode"></a>Режим без окон VMR

Режим без окон — это предпочтительный способ отображения видео в окне приложения. В режиме без окон модуль подготовки видео не загружает свой компонент диспетчера окон и поэтому не поддерживает интерфейсы [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) и [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) . Вместо этого приложение предоставляет окно воспроизведения и задает прямоугольник назначения в клиентской области для изображения VMR, чтобы нарисовать видео. VMR использует объект DirectDraw Clipper, чтобы убедиться, что видео обрезано в окне приложения и не отображается в других окнах. VMR не подклассует окно приложения или устанавливает обработчики систем и процессов.

В режиме без окон последовательность событий во время соединения и перехода в состояние выполнения выглядит следующим образом:

-   Вышестоящий фильтр предлагает тип мультимедиа, который VMR принимает или отклоняет.
-   Если тип мультимедиа принимается, VMR вызывает средство распределителя-Presenter для получения поверхности DirectDraw. Если поверхность создана успешно, то контакты соединяются, а фильтр VMR готов к переходу в состояние выполнения.
-   При запуске графа фильтра декодер вызывает метод " **buffer** " для получения примера мультимедиа из распределителя. VMR запрашивает устройство распределителя, чтобы убедиться, что глубина пикселя, размер прямоугольника и другие параметры на поверхности DirectDraw совместимы с входящим видео. Если они совместимы, то VMR возвращает для декодера поверхность DirectDraw. После декодирования декодера в области основной модуль синхронизации VMR проверяет отметки времени. Эта единица блокирует вызов **Receive** до наступления времени презентации. На этом этапе VMR вызывает **пресентимаже** для распределителя-Presenter, который представляет поверхность для графической карты.

На следующем рисунке показан фильтр VMR в режиме без окон с несколькими входными потоками.

![VMR в режиме без окон](images/vmr-windowless-mult-streams.png)

**Настройка VMR-7 для режима без окон**

Чтобы настроить VMR-7 для режима без окон, перед подключением любых входных ПИН-кодов VMR выполните все описанные ниже действия.

1.  Создайте фильтр и добавьте его в граф.
2.  Вызовите метод [**ивмрфилтерконфиг:: сетрендерингмоде**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) с \_ неоконным флагом вмрмоде.
3.  При необходимости настройте VMR для нескольких входных потоков, вызвав [**ивмрфилтерконфиг:: сетнумберофстреамс**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). VMR создает ПИН-код входа для каждого потока. Используйте интерфейс [**ивмрмиксерконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) , чтобы задать Z-порядок и другие параметры для потока. дополнительные сведения см. [в разделе VMR с несколькими Потокиами (режим смешения)](vmr-with-multiple-streams--mixing-mode.md).

    Если не вызвать **сетнумберофстреамс**, VMR-7 по умолчанию принимает один входной ПИН-код. После подключения входных контактов число ПИН-кодов не может быть изменено.

4.  Вызовите метод [**ивмрвиндовлессконтрол:: сетвидеоклиппингвиндов**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) , чтобы указать окно, в котором будет отображаться отображаемое видео.

После выполнения этих действий можно подключить входные сигналы фильтра VMR. существует несколько способов создания графа, таких как соединение закрепления напрямую, с помощью интеллектуальных Подключение методов, таких как [**играфбуилдер:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), или с помощью метода [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) построителя Graph. Дополнительные сведения см. в разделе [общие Graph-Building методы](general-graph-building-techniques.md).

Чтобы задать расположение видео в окне приложения, вызовите метод [**ивмрвиндовлессконтрол:: сетвидеопоситион**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) . Метод [**ивмрвиндовлессконтрол:: жетнативевидеосизе**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) возвращает собственный размер видео. во время воспроизведения приложение должно уведомлять VMR о следующих Windows сообщениях:

-   WM \_ Paint: вызов [**ивмрвиндовлессконтрол:: репаинтвидео**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) для перерисовки изображения.
-   WM \_ дисплайчанже: Call [**ивмрвиндовлессконтрол::D исплаймодечанжед**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). VMR выполняет все действия, необходимые для показа видео с новым разрешением или глубиной цвета.
-   Размер WM: повторное \_ Вычисление расположения видео и вызов [**сетвидеопоситион**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) при необходимости.

> [!Note]  
> Приложения MFC должны определять пустой \_ обработчик сообщений WM ерасебкгнд, иначе область видеоизображения не будет правильно перерисовываться.

 

**Настройка VMR-9 для режима без окон**

Чтобы настроить VMR-9 для режима без окон, выполните действия, описанные в разделе VMR-7 для режима без окон, но используйте интерфейсы [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) и [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) . Единственная существенная разница заключается в том, что VMR-9 создает четыре входных контакта по умолчанию, а не один входной ПИН-код. Поэтому необходимо вызвать **сетнумберофстреамс** только в том случае, если используется более четырех потоков видео.

**Пример кода**

в следующем коде показано, как создать фильтр VMR-7, добавить его в граф фильтра DirectShow, а затем перевести VMR в режим без окон. Для VMR-9 используйте CLSID \_ VideoMixingRenderer9 в **CoCreateInstance** и соответствующие интерфейсы VMR-9.


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование режима без окон](using-windowless-mode.md)
</dt> </dl>

 

 



