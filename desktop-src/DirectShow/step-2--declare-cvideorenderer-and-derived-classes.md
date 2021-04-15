---
description: В этом разделе описывается шаг 2 руководства воспроизведение аудио-и видеороликов в DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: Шаг 2. объявление Квидеорендерер и производных классов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11474c57e70d8632a53ac0b858d61d2bddf1e86b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683991"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a>Шаг 2. объявление Квидеорендерер и производных классов

В этом разделе описывается шаг 2 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md). Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).

DirectShow предоставляет несколько различных фильтров, которые визуализируют видео:

-   [**Расширенный фильтр модуля подготовки**](enhanced-video-renderer-filter.md) отчетов (Евр)
-   [Фильтр прорисовки видео 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Фильтр визуализации 7 для микширования видео](video-mixing-renderer-filter-7.md) (VMR-7)

Дополнительные сведения о различиях между этими фильтрами см. [в разделе Выбор правильного модуля подготовки видео](choosing-the-right-renderer.md).

В этом руководстве приведен следующий абстрактный класс, используемый для упаковки фильтра модуля подготовки отчетов.


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



Примечания.

-   `HasVideo`Метод возвращает **значение true** , если модуль подготовки видео создан.
-   `AddToGraph`Метод добавляет модуль подготовки видео к графу фильтра.
-   `FinalizeGraph`Метод завершает шаг построения графа.
-   `UpdateVideoWindow`Метод обновляет прямоугольник назначения видео.
-   `Repaint`Метод перерисовывает текущий кадр видео.
-   `DisplayModeChanged`Метод обрабатывает изменения режима просмотра.

Каждый из этих методов подробно описан далее в этом руководстве.

Затем объявите производный класс для создания оболочки для каждого из трех модулей подготовки видео: ЕВР, VMR-9 и VMR-7.

### <a name="cevr-class"></a>Класс ЦЕВР

`CEVR`Класс управляет Евр. Он содержит указатель на интерфейсы [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) и [**имфвидеодисплайконтрол**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) Евр.


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a>Класс CVMR9

`CVMR9`Класс управляет фильтром VMR-9. Он содержит указатель на интерфейс [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a>Класс CVMR7

`CVMR7`Класс управляет фильтром VMR-7. Он содержит указатель на интерфейс [**ивмрвиндовлессконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



Далее: [Шаг 3. Построение графа фильтра](step-3--build-the-filter-graph.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Воспроизведение звука и видео в DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md)
</dt> <dt>

[Рендеринг видео](video-rendering.md)
</dt> </dl>

 

 
