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
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a><span data-ttu-id="edb89-103">Шаг 2. объявление Квидеорендерер и производных классов</span><span class="sxs-lookup"><span data-stu-id="edb89-103">Step 2: Declare CVideoRenderer and Derived Classes</span></span>

<span data-ttu-id="edb89-104">В этом разделе описывается шаг 2 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="edb89-104">This topic is step 2 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="edb89-105">Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="edb89-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="edb89-106">DirectShow предоставляет несколько различных фильтров, которые визуализируют видео:</span><span class="sxs-lookup"><span data-stu-id="edb89-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="edb89-107">[**Расширенный фильтр модуля подготовки**](enhanced-video-renderer-filter.md) отчетов (Евр)</span><span class="sxs-lookup"><span data-stu-id="edb89-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="edb89-108">[Фильтр прорисовки видео 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="edb89-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="edb89-109">[Фильтр визуализации 7 для микширования видео](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="edb89-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="edb89-110">Дополнительные сведения о различиях между этими фильтрами см. [в разделе Выбор правильного модуля подготовки видео](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="edb89-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="edb89-111">В этом руководстве приведен следующий абстрактный класс, используемый для упаковки фильтра модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="edb89-111">In this tutorial, the following abstract class is used to wrap the video renderer filter.</span></span>


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



<span data-ttu-id="edb89-112">Примечания.</span><span class="sxs-lookup"><span data-stu-id="edb89-112">Notes:</span></span>

-   <span data-ttu-id="edb89-113">`HasVideo`Метод возвращает **значение true** , если модуль подготовки видео создан.</span><span class="sxs-lookup"><span data-stu-id="edb89-113">The `HasVideo` method returns **TRUE** if the video renderer has been created.</span></span>
-   <span data-ttu-id="edb89-114">`AddToGraph`Метод добавляет модуль подготовки видео к графу фильтра.</span><span class="sxs-lookup"><span data-stu-id="edb89-114">The `AddToGraph` method adds the video renderer to the filter graph.</span></span>
-   <span data-ttu-id="edb89-115">`FinalizeGraph`Метод завершает шаг построения графа.</span><span class="sxs-lookup"><span data-stu-id="edb89-115">The `FinalizeGraph` method completes the graph-building step.</span></span>
-   <span data-ttu-id="edb89-116">`UpdateVideoWindow`Метод обновляет прямоугольник назначения видео.</span><span class="sxs-lookup"><span data-stu-id="edb89-116">The `UpdateVideoWindow` method updates the video destination rectangle.</span></span>
-   <span data-ttu-id="edb89-117">`Repaint`Метод перерисовывает текущий кадр видео.</span><span class="sxs-lookup"><span data-stu-id="edb89-117">The `Repaint` method redraws the current video frame.</span></span>
-   <span data-ttu-id="edb89-118">`DisplayModeChanged`Метод обрабатывает изменения режима просмотра.</span><span class="sxs-lookup"><span data-stu-id="edb89-118">The `DisplayModeChanged` method handles display-mode changes.</span></span>

<span data-ttu-id="edb89-119">Каждый из этих методов подробно описан далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="edb89-119">Each of these methods is described in detail later in this tutorial.</span></span>

<span data-ttu-id="edb89-120">Затем объявите производный класс для создания оболочки для каждого из трех модулей подготовки видео: ЕВР, VMR-9 и VMR-7.</span><span class="sxs-lookup"><span data-stu-id="edb89-120">Next, declare a derived class to wrap each of the three video renderers: the EVR, the VMR-9, and the VMR-7.</span></span>

### <a name="cevr-class"></a><span data-ttu-id="edb89-121">Класс ЦЕВР</span><span class="sxs-lookup"><span data-stu-id="edb89-121">CEVR Class</span></span>

<span data-ttu-id="edb89-122">`CEVR`Класс управляет Евр.</span><span class="sxs-lookup"><span data-stu-id="edb89-122">The `CEVR` class manages the EVR.</span></span> <span data-ttu-id="edb89-123">Он содержит указатель на интерфейсы [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) и [**имфвидеодисплайконтрол**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) Евр.</span><span class="sxs-lookup"><span data-stu-id="edb89-123">It contains a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) and [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interfaces of the EVR.</span></span>


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



### <a name="cvmr9-class"></a><span data-ttu-id="edb89-124">Класс CVMR9</span><span class="sxs-lookup"><span data-stu-id="edb89-124">CVMR9 Class</span></span>

<span data-ttu-id="edb89-125">`CVMR9`Класс управляет фильтром VMR-9.</span><span class="sxs-lookup"><span data-stu-id="edb89-125">The `CVMR9` class manages the VMR-9.</span></span> <span data-ttu-id="edb89-126">Он содержит указатель на интерфейс [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="edb89-126">It contains a pointer to the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>


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



### <a name="cvmr7-class"></a><span data-ttu-id="edb89-127">Класс CVMR7</span><span class="sxs-lookup"><span data-stu-id="edb89-127">CVMR7 Class</span></span>

<span data-ttu-id="edb89-128">`CVMR7`Класс управляет фильтром VMR-7.</span><span class="sxs-lookup"><span data-stu-id="edb89-128">The `CVMR7` class manages the VMR-7.</span></span> <span data-ttu-id="edb89-129">Он содержит указатель на интерфейс [**ивмрвиндовлессконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="edb89-129">It contains a pointer to the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>


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



<span data-ttu-id="edb89-130">Далее: [Шаг 3. Построение графа фильтра](step-3--build-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="edb89-130">Next: [Step 3: Build the Filter Graph](step-3--build-the-filter-graph.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="edb89-131">См. также</span><span class="sxs-lookup"><span data-stu-id="edb89-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edb89-132">Воспроизведение звука и видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="edb89-132">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="edb89-133">Использование модуля подготовки видео для микширования</span><span class="sxs-lookup"><span data-stu-id="edb89-133">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="edb89-134">Рендеринг видео</span><span class="sxs-lookup"><span data-stu-id="edb89-134">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
